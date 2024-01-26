<script lang="ts">
  import { Canvas } from '@threlte/core'
  import Scene from './DemoScene.svelte'
  import Header from '$lib/components/Header.svelte';
</script>

<div style="flex-grow: 1;">
  <Canvas>
    <Scene />
  </Canvas>
</div>