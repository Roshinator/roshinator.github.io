<script lang="ts">
	import { createEventDispatcher, onMount } from "svelte";
	import { slide } from "svelte/transition";

	export let name:string;

	let ready = false;
	onMount(() =>
	{
		ready = true;
	})

	const dispatch = createEventDispatcher();
	function finishIntro()
	{
		dispatch('complete')
	}
</script>

<div class="header-background">
	<div class="h-flow">
		<h1>Roshinator:&nbsp;</h1>
		{#if ready}
			<h1 transition:slide={{delay:750, duration:1000, axis: 'x'}}>{name}</h1>
		{/if}
	</div>


	<div class="nav-menu">
		<a href="/">Home</a>
		<a href="/about">About</a>
	</div>
</div>

<style>
	.header-background {
		text-align: center;
		padding: 20px;
	}

	a {
		font-family: Inter, Arial, Helvetica, sans-serif;
	}

	.nav-menu {
		
	}
</style>