<script lang="ts">
  import { FeedbackStore } from "./stores";
  import FeebackList from "./components/FeebackList.svelte";
  import FeedbackStats from "./components/FeedbackStats.svelte";
  import FeedbackForm from "./components/FeedbackForm.svelte";

  const addFeedback = (e: any) => {
    FeedbackStore.update((curr) => {
      return [e.detail, ...curr];
    });
  };
</script>

<main class="container">
  <FeedbackForm on:submit-data={addFeedback} />
  <FeedbackStats />
  <FeebackList />
</main>

<style>
</style>
