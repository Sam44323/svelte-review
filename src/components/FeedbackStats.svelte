<script lang="ts">
  import { FeedbackStore } from "src/stores";
  $: count = $FeedbackStore.length; // reactive value i.e. will change based on dependent value
  $: average = $FeedbackStore.reduce((a, b) => a + b.rating, 0) / count;
</script>

<div class="feedback-stats">
  <h4>{count} Reviews</h4>
  <h4>Ratings Average : {average}</h4>
</div>

<style>
  .feedback-stats {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
</style>
