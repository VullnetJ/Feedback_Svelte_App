<script>
    export let style ='primary'
    export let type = 'button'
    export let disabled = false
</script>

<button {type} {disabled} class={style}>
    <slot></slot>
</button>

<style>
    button {
        color:palevioletred;
        border: 0;
        border-radius: 8px;
        color: burlywood;
        width: 100px;
        height: 42px;
        cursor: pointer;
    }
    .primary {
        background-color: rgb(29, 16, 16);
    }
    .secondary {
        background-color: indianred;
    }
    button:hover {
        transform: scale(0.96);
        opacity: 0.9;
    }
    button:disabled {
        background-color: grey;
        color: rgb(44, 38, 38);
    }
</style>