<script lang="ts">
    import Mail from "lucide-svelte/icons/mail";
    import { Button } from "$lib/components/ui/button"
</script>

<h1 class="text-3xl font-bold underline">Welcome to SvelteKit</h1>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>

<Button variant="outline" onclick={()=>alert("Hello")}>
    <Mail class="mr-2 size-4" />
    Button
</Button>