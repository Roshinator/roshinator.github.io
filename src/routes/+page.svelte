<script lang="ts">
	import "./styles.css";

	import {onMount} from 'svelte';
	import {fly} from 'svelte/transition';

	import NavItem from "./NavItem.svelte";

	let ready = false;
	onMount(() => ready = true)
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="flex-root page-size no-shrink">
	<div class="header-background">
		<h1>
			Title
		</h1>
	</div>

{#if ready}
	<div class="item-root" transition:fly={{y: 50, duration:1000}}>
		<div class="nav no-shrink">
			<NavItem />
		</div>
		<div class="view">

		</div>
	</div>
{/if}

</div>



<style>

	.item-root {
		height: 100%;
		flex-shrink: 100000;
		display: flex;
		flex-direction: row;

		border: 1px solid black;
		margin-left: 10px;
		margin-right: 10px;
		margin-bottom: 5px;

		background-color: red;
	}

	.nav {
		width: 400px;
		height: 100%;

		border-right: 1px solid black;
	}

	.view {
		width: 100%;
		height: 100%;
		flex-shrink: 100;

	}

</style>
