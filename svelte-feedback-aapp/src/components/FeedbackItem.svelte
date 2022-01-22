<script>
    // import {createEventDispatcher} from 'svelte'
    import {FeedbackStore} from '../stores'

    import Card from './Card.svelte'
    export let item 

    // const dispatch = createEventDispatcher()

    const handleDelete = (itemId) => {
        // dispatch('delete-feedback', itemId)
        FeedbackStore.update((currentFeedback) => {
            return currentFeedback.filter(item => item.id !=itemId)
        })
    }
</script>

<Card>
    <div class="num-display">
        {item.rating}
    </div>
    <button class="close" on:click ={() => handleDelete(item.id)}>X</button>
    <p class="text-display">
        {item.text}
    </p>
</Card>

<style>
    .num-display {
        position: absolute;
        top: -10px;
        left: -10px;
        width: 55px;
        height: 55px;
        background-color: rgb(202, 74, 185);
        color: rgb(216, 216, 221);
        border: 1px rgb(54, 15, 117) solid;
        border-radius: 50%;
        padding: 10px;
        text-align: center;
        font-size: 20px;
    }
    .close   {
        position: absolute;
        top: 10px;
        right: 10px;
        cursor: pointer;
        background: none;
        border: none;
    }
</style>