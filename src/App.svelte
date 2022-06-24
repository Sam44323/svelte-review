<script lang="ts">
  import FeebackList from "./components/FeebackList.svelte";
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

  const deleteFeedback = (e) => {
    feedback = feedback.filter((item) => item.id !== e.detail);
  };
</script>

<main class="container">
  <FeebackList feedbackData={feedback} on:delete-feedback={deleteFeedback} />
</main>

<style>
</style>
