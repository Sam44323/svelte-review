<script lang="ts">
  import { FeedbackStore } from "./stores";
  import FeebackList from "./components/FeebackList.svelte";
  import FeedbackStats from "./components/FeedbackStats.svelte";
  import FeedbackForm from "./components/FeedbackForm.svelte";
  import FeebackItem from "./components/FeebackItem.svelte";

  $: count = $FeedbackStore.length; // reactive value i.e. will change based on dependent value
  $: average = $FeedbackStore.reduce((a, b) => a + b.rating, 0) / count;

  const addFeedback = (e: any) => {
    FeedbackStore.update((curr) => {
      return [e.detail, ...curr];
    });
  };
</script>

<main class="container">
  <FeedbackForm on:submit-data={addFeedback} />
  <FeedbackStats {count} {average} />
  <FeebackList />
</main>

<style>
</style>
