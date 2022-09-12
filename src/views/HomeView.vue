<script>
export default {
  data: function () {
    return {
      message: "Welcome to Vue.js!",
      words: ["other", "lunch", "horse", "maybe", "spare", "reads", "stone", "dog"],
      word: "",
      guessOne: "lunch",
      evaluation: [0, 0, 0, 0, 0]
    };
  },
  created: function () {
    this.pickWord()
  },
  methods: {
    pickWord: function () {
      this.word = this.words[Math.floor(Math.random() * this.words.length)];
      this.word = this.word.split('')
    },
    checkWord: function (guess) {
      //   console.log("checking word")
      //   guess = guess.split('')
      //   guess.forEach(function (letter, index) => {
      //     console.log(this.word)
      //     console.log(letter)
      //     index++
      //   })
      // console.log(this.evaluation)
    }
  },
};
</script>

<template>
  <div class="home">
    <h1>{{ message }}</h1>
    <p>{{word}}</p>
    <h2>Enter a guess</h2>
    <!-- <input type="text" v-model="guessOne"> -->
    <button v-on:click="checkWord(guessOne)">Run checkWord</button>

  </div>
</template>

<style>

</style>