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
    <hr>
    <p>v-for :key v-bind</p>
<a v-bind:href="url">google.com v-bind:href dynamic classes</a>

<div v-if="showBooks">
  <ul>
    <!-- adding class 'fav' if b.isFav=true -->
    <li v-for="b in books" :key="b.id" v-bind:class="{ fav: b.isFav}" @click="toggleFav(b)">
      <!-- not showing images, wrong path ? changed to b.title, so it could show alt attribute -->
      <img v-bind:src="b.title" v-bind:alt="b.title">
      <h3>{{ b.title }}</h3>
      <p>{{ b.author }}</p>
    </li>
  </ul>
  <!-- not sure if this key should be value.id ?  -->
  <p v-for="(value, key) in books" :key="value.id">
  value {{ value }} key {{ key }} </p>
</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "Pav",
      age: 34,
      visible: true,
      showBooks: true,
      books: [
        {title: "title two", author: 'author of title two', img: '1.jpg', isFav: true},
        {title: "title three", author: 'author of title three', img: '../assets/img/2.jpg', isFav: true},
        {title: "title four", author: 'author of title four', img: '../assets/img/1.jpg', isFav: false},
        {title: "title one", author: 'author of title one', img: '../assets/img/2.jpg', isFav: true},
      ],
      url: "https://www.google.com"
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
      this.visible = !this.visible
    },
    toggleShowBooks() {
      this.showBooks = !this.showBooks
    },
    // asd or any other name for this arg, but it is my b in books
    toggleFav(asd) {
      asd.isFav = !asd.isFav
    }
  },
};
</script>

<style>
   
    body{
      background: #eee;
      max-width: 960px;
      margin: 20px auto;
    }
    li{
      list-style-type: none;
      background: #fff;
      margin: 20px auto;
      padding: 10px 20px;
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    li.fav{
      background: #ff9ed2;
      color: white;
    }
    a:hover{
      cursor: pointer;
    }
  
</style>