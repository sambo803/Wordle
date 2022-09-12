<script>
export default {
  data: function () {
    return {
      message: "Welcome to Vue.js!",
      words: ["other", "lunch", "horse", "maybe", "spare", "reads", "stone"],
      word: ""
    };
  },
  created: function () {
    this.pickWord()
  },
  methods: {
    pickWord: function () {
      this.word = this.words[Math.floor(Math.random() * this.words.length)];
    }
  },
};
</script>

<template>
  <div class="home">
    <h1>{{ message }}</h1>
    <p>{{word}}</p>
  </div>
</template>

<style>

</style>