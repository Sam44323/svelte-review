<script lang="ts">
  import FeebackList from "./components/FeebackList.svelte";
  import FeedbackStats from "./components/FeedbackStats.svelte";

  let feedback = [
    {
      id: 1,
      rating: 10,
      text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. consequuntur vel vitae commodi alias voluptatem est voluptatum ipsa quae.",
    },
    {
      id: 2,
      rating: 9,
      text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. consequuntur vel vitae commodi alias voluptatem est voluptatum ipsa quae.",
    },
    {
      id: 3,
      rating: 8,
      text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. consequuntur vel vitae commodi alias voluptatem est voluptatum ipsa quae.",
    },
  ];

  $: average = feedback.reduce((a, b) => a + b.rating, 0) / feedback.length; // reactive value i.e. will change based on dependent value

  const deleteFeedback = (e: any) => {
    feedback = feedback.filter((item) => item.id !== e.detail);
  };
</script>

<main class="container">
  {average}
  <FeebackList feedbackData={feedback} on:delete-feedback={deleteFeedback} />
</main>

<style>
</style>
