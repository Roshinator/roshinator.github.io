<script lang="ts">
    import '$lib/fonts/cascadiacode.css';

    type HEX = `#${string}`;

    export let name:string; 
    export let listId:string;
    export let color: HEX;
    export let checked:boolean = false;

    let checkedHtml:string;
    $: if (checked) {
        checkedHtml = "checked";
    }
    else {
        checkedHtml = "";
    }
</script>

<label class="container">
    <input type="radio" name="{listId}" value="{name}" {checked}>
    <span style="--bg-col: {color};" class="background"></span>
    <p>{name}</p>
</label>


<style>

    .container {
        margin: 0px;
        padding: 0px;
        width: 100%;
        height: 50px;
        border-bottom: 2px solid black;
        display: flex;
        user-select: none;

        font-family: CascadiaCode, monospace;
        font-size: 18px;
        position: relative;
    }

    .background {
        width: 0%;
        height: 100%;

        background-color: var(--bg-col);
        transition: width 100ms ease;
    }

    p {
        position: absolute;
        top: 50%;
        left: 20px;
        transform: translate(0%, -50%);
        margin: 0px;
        padding: 4px;
        text-decoration: underline 0.15em #000000;
    }

    .container input {
        position: absolute;
        opacity: 0;
        cursor: pointer;
        height: 0;
        width: 0;
    }

    .container:hover > .background {
        width: 16px;
    }

    .container input:checked ~ .background {
        width: 100%
    }

</style>