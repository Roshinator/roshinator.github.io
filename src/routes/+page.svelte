<script lang="ts">
	import "./styles.css";

	import NavItem from "./NavItem.svelte";
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="item-root">
	<div class="nav no-shrink">
		<div class="scroll-area">
			<NavItem name={"Tankken"} listId={"projectlist"} color="#ff94a4" checked/> 
			<NavItem name={"Game Boy Inator"} color="#ffee93" listId={"projectlist"}/> 
			<NavItem name={"GEDCOM Viewer"} color="#93ffee" listId={"projectlist"}/> 
			<NavItem name={"CrossCorrupt"} color="#93a3ff" listId={"projectlist"}/> 
		</div>
	</div>
	<div class="view">

	</div>
</div>



<style>

	.no-shrink {
	    flex-shrink: 0;
    }

    .flex-root {
        /*background-color: #FF94A4;*/
        display: flex;
        align-items: stretch;
        justify-content: top;
        flex-direction: column;
    }

    .page-size {
        height: 100%;
    }

	.item-root {
		height: 100%;
		flex-shrink: 100000;
		display: flex;
		flex-direction: row;

		border: 2px solid black;
		margin-left: 10px;
		margin-right: 10px;
		margin-bottom: 5px;

		border-radius: 10px;
		overflow: hidden;
	}

	.scroll-area {
		height: 100%;
		overflow: scroll;
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
