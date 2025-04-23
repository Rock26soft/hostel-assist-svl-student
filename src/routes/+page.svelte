<script>
    import './root.css';
    import '../app.css';
    import { goto } from '$app/navigation';
    export let name = "Hostel Assist";
    export let status = "Getting things ready..."
    import { onMount } from 'svelte';

    onMount(() => {
        setTimeout(() => {
            goto('/login');
        }, 2000);
    });
</script>


<div class="flex content-center flex-col items-center justify-center place-content-center h-svh mobile">
    <div class="h-50 w-50 splash_shadow splash_container">
        <img src="logo.png" alt="logo">
    </div>
    <p class="m-5 title">{name}</p>
    <p class="m-5 title description">{status}</p>
</div>
