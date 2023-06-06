<script>
    import { Capacitor } from "@capacitor/core";
	import { StatusBar, Style } from '@capacitor/status-bar';
    import { onMount } from 'svelte';

	onMount(async () => {
		if (Capacitor.isPluginAvailable('StatusBar') && Capacitor.getPlatform() !== 'web'){
            StatusBar.setBackgroundColor({
                color: "#ff715b"
            })
            StatusBar.setOverlaysWebView({ overlay: true });
		}
	});
</script>
<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
<style>
    :global(body){
        background-color: #ff715b;
        color: #ffffff;
    }
</style>