<script>
    import {FeedbackStore} from '../stores'
   
    $: count = $FeedbackStore.length
	$: average = $FeedbackStore.reduce((a, {rating}) => a + rating, 0 ) / count

</script>

<div class="feedback-stats">
    <h3>{count} Reviews</h3>
    <h3>Rating Average: {average} </h3>
</div>

<style>
    .feedback-stats {
        display: flex;
        justify-content:space-between;
        align-items: center;
    }
</style>
