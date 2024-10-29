<script lang="ts">
  import { ModeWatcher } from "mode-watcher";
  import { toggleMode } from "mode-watcher";
  import { Button } from "$lib/components/ui/button"
  import SunMoon from "../../node_modules/lucide-svelte/dist/icons/Sun-moon.svelte";
  import * as Resizable from "$lib/components/ui/resizable";

  import '../app.css';
  let { children } = $props();

</script>

<ModeWatcher />

<div class="container ">

  <Button onclick={toggleMode} variant="outline">
    <SunMoon /> Dark/Light
  </Button>

<Resizable.PaneGroup 
  direction="vertical"
  class="min-h-[800px] rounded-lg border">

  <Resizable.Pane
    defaultSize={6} >
    <div class="flex h-full items-center justify-center p-6">
    <span class="font-semibold">HEADER</span>
    </div>
  </Resizable.Pane>

  <Resizable.Handle />

  <Resizable.Pane>


	<Resizable.PaneGroup direction="horizontal"> 
      <Resizable.Pane 
	  	defaultSize={20}>
        <div class="flex h-full items-center justify-center p-6">
          <span class="font-semibold">LEFT ASIDE</span>
        </div>
      </Resizable.Pane>
      <Resizable.Handle withHandle />
      <Resizable.Pane >
        <div class="flex h-full items-center justify-center p-6">
          <span class="font-semibold">MAIN</span>
        </div>
      </Resizable.Pane>
      <Resizable.Handle withHandle />
      <Resizable.Pane 
	  	defaultSize={6}>
        <div class="flex h-full items-center justify-center p-6">
          <span class="font-semibold">RIGHT ASIDE</span>
        </div>
      </Resizable.Pane>
    </Resizable.PaneGroup>

  </Resizable.Pane>

  <Resizable.Handle />
  
  <Resizable.Pane
    defaultSize={6} >
    <div class="flex h-full items-center justify-center p-6">
    <span class="font-semibold">FOOTER</span>
    </div>
  </Resizable.Pane>

</Resizable.PaneGroup>

</div>


  
