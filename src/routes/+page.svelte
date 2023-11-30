<script lang="ts">
	import "./styles.css";

	import NavItem from "./NavItem.svelte";
	import Header from "./Header.svelte";
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<Header name={"Projects"}/>

<div class="item-root">
	<div class="nav no-shrink">
		<NavItem name={"Tankken"}/> 
		<NavItem name={"Game Boy Inator"}/> 
		<NavItem name={"GEDCOM Viewer"}/> 
		<NavItem name={"CrossCorrupt"}/> 
	</div>
	<div class="view">

	</div>
</div>



<style>

	.item-root {
		height: 100%;
		flex-shrink: 100000;
		display: flex;
		flex-direction: row;

		border: 2px solid black;
		margin-left: 10px;
		margin-right: 10px;
		margin-bottom: 5px;

		
	}

	.nav {
		width: 400px;
		height: 100%;

		border-right: 2px solid black;
	}

	.view {
		width: 100%;
		height: 100%;
		flex-shrink: 100;

	}

</style>
