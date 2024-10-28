<script lang="ts">
    import { toggleMode } from "mode-watcher";
    import { Button } from "$lib/components/ui/button"

    import SunMoon from "../../node_modules/lucide-svelte/dist/icons/Sun-moon.svelte";
    
</script>

<h1 class="text-3xl font-bold underline">Welcome to SvelteKit</h1>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>

<Button onclick={toggleMode} variant="outline">
    <SunMoon /> Dark/Light
</Button>