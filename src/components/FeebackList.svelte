<script lang="ts">
  import FeebackItem from "./FeebackItem.svelte";
  export let feedbackData = []; // will be props (if anything is not passed, then it'll be the default data)

  console.log(feedbackData);
</script>

<main>
  {#each feedbackData as fData (fData.id)}
    <FeebackItem item={fData} />
  {/each}
</main>

<style></style>
