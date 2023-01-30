<template>
  <div>
    <p>Functions</p>
    <section>
      <h2>My course Goal</h2>
      <p>{{ courseGoal }}</p>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      courseGoal: "To finish course!",
    };
  },
};
</script>
