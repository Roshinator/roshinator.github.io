<script>
    import Header from '$lib/components/Header.svelte';
</script>

<div>
    <Header/>
    <slot/>
</div>

<style>
    div {
        display: flex;
        flex-direction: column;
        height: 100%;
    }
</style>
