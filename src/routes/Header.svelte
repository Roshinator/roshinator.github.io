<script lang="ts">
	export let name:string;
</script>

<div class="header-background">
	<h1>
		Roshinator: {name}
	</h1>

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