<template>
  <div>
    <button @click="toggleShow">
      <span v-if="visible">Hide</span>
      <!-- <span v-if="!visible">Show</span> -->
      <span v-else>Show</span>
    </button>
    <div v-if="visible">
      <p>My name is {{ name }} and I am {{ age }} years</p>
    </div>
    <button v-on:click="age++">age +1</button>
    <button @click="age--">age -1</button>
    <button @click="toggleName">Change name</button>
    <p v-show="!visible">Click show to see.</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "Pav",
      age: 34,
      visible: true,
    };
  },
  methods: {
    toggleName() {
      if (this.name == "Pav") {
        this.name = "Sophie";
      } else {
        this.name = "Pav";
      }
    },
    toggleShow() {
      this.visible = !this.visible;
    },
  },
};
</script>
