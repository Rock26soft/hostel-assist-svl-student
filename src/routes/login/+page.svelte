<script>
	import "../root.css"
	import "../../app.css"
	import { blur } from 'svelte/transition';
	import { Button, GradientButton } from 'flowbite-svelte';
	import { Toast } from 'flowbite-svelte';
	import { ExclamationCircleOutline } from 'flowbite-svelte-icons';
	//check login status else
</script>
<style>
    .logo-small {
        height: auto;
        width: 120px;

        @media (min-width: 640px) {
            width: 160px;
        }

        @media (min-width: 1024px) {
            width: 170px;
        }
				margin: 10px;
    }
		.top-bar{
        position: relative;
				display: flex;
				flex-direction: column;
				padding-top: 40px;
				align-items: center;
				height: 100vh;
				width: 100%;
				padding-bottom: 120px;
				backdrop-filter: blur(20px);
        background: linear-gradient(90deg, var(--primary), var(--secondary));
		}
		.login-box{
				position: absolute;
				bottom: -40px;
				height: 60vh;
				width: 100%;
				display: flex;
				flex-direction: column;
        padding-top:100px;
				align-items: center;
				transform: translateY(-40px);
				background-color: white;
				border-top-left-radius: 25px;
				border-top-right-radius: 25px;
				animation: slide-up 0.6s ease-in-out;
		}

		@keyframes slide-up {
				0%{
						transform: translateY(400px);
				}
				100%{
						transform: translateY(-40px);
        }
    }
</style>
<div class="relative flex content-center justify-between flex-col h-svh mobile">
	<div class="top-bar">
		<img src="logo.png" class="logo-small" alt="logo">
		<p style="color: var(--purple-200);font-size: 1.6em">Hostel Assist</p>
		<p style="color: var(--purple-200);font-size: 1.2em">Student Login</p>
	</div>
	<div class="login-box">
		<p>Login with MANIT Gmail ID</p>
		<Button class="relative w-60 m-5" >Google login</Button>
		<Toast transition={blur} params={{ amount: 50,delay:20 }} class="transform translate-y-10">
			<ExclamationCircleOutline slot="icon" class="w-6 h-6 text-primary-500 bg-primary-100 dark:bg-primary-800" />
			Only login with scholar_number@stu.manit.ac.in Google ID
		</Toast>
	</div>
</div>
