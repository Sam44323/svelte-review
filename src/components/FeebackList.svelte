<script lang="ts">
  import FeebackList from "./FeebackList.svelte";
  import FeebackItem from "./FeebackItem.svelte";
  export let feedbackData = []; // will be props (if anything is not passed, then it'll be the default data)

  console.log(feedbackData);
</script>

<main>
  {#each feedbackData as fData (fData.id)}
    <h3>{fData.text}</h3>
    <FeebackItem />
  {/each}
</main>

<style></style>
