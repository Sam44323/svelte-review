<script lang="ts">
  import { FeedbackStore } from "./stores";
  import FeebackList from "./components/FeebackList.svelte";
  import FeedbackStats from "./components/FeedbackStats.svelte";
  import FeedbackForm from "./components/FeedbackForm.svelte";
</script>

<main class="container">
  <FeedbackForm />
  <FeedbackStats />
  <FeebackList />
</main>

<style>
</style>
