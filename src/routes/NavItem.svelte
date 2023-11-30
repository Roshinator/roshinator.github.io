<script lang="ts">
    import '$lib/fonts/Cascadia Code/cascadiacode.css';

    export let name:string; 
</script>

<div class="item-box">
    <p>{name}</p>
</div>


<style>

    .item-box {
        margin: 0px;
        padding: 0px;
        border-bottom: 2px solid black;
    }

    p {
        margin: 0px;
        padding: 20px;
        font-family: CascadiaCode, monospace;
        font-size: 18px;

        text-decoration: underline 0.15em #000000;
        transition: text-decoration-color 200ms;
    }

    p:hover {
        text-decoration-color: #FF94A4;
    }

</style>