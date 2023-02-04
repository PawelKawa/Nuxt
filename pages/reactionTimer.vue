<template>
  <div class="h-96 bg-zinc-200">
    <p class="text-center">Reaction Timer</p>
    <div class="flex justify-center">
        <button :disabled="isPlaying" @click="start">
            start
        </button>
    </div>
    <block v-if="isPlaying" :delay="delay" @end="endGame" />
    <results v-if="showResults" :scorE="score" />
  </div>
</template>

<script>
import block from "../components/reactionTimer/block.vue";
import results from "../components/reactionTimer/result.vue";

export default {
  name: "reaction",
  components: {
      block,
    results,
  },
  data() {
    return {
      isPlaying: false,
      delay: null,
        score: null,
      showResults: false,
    };
  },
  methods: {
    start() {
      this.delay = 1000 + Math.random() * 4000;
      this.isPlaying = true;
      this.showResults = false;
    },
    endGame(reactionTime) {
      this.score = reactionTime;
        this.isPlaying = false;
        this.showResults = true;
    },
  },
};
</script>
