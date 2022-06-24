<script lang="ts">
  import { scale, fade } from "svelte/transition";
  import { FeedbackStore } from "../stores";

  import FeebackItem from "./FeebackItem.svelte";
</script>

<main>
  {#each $FeedbackStore as fData (fData.id)}
    <div in:scale out:fade={{ duration: 500 }}>
      <FeebackItem item={fData} />
    </div>
  {/each}
</main>

<style></style>
