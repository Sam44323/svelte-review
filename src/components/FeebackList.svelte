<script lang="ts">
  import { scale, fade } from "svelte/transition";

  import FeebackItem from "./FeebackItem.svelte";
  export let feedbackData = []; // will be props (if anything is not passed, then it'll be the default data)

  console.log(feedbackData);
</script>

<main>
  {#each feedbackData as fData (fData.id)}
    <div in:scale out:fade={{ duration: 500 }}>
      <FeebackItem item={fData} on:delete-feedback />
    </div>
  {/each}
</main>

<style></style>
