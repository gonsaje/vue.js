/*
From my understanding Vue breaks down its architecture
into 3 portions
template: HTML
script: JavaScript
style: CSS
*/


// Use HTML Elements for UI 
<template>
  <div>
    <img id="logo" src="../assets/pisrclogo.jpeg" />
    <h1 class="h1-title">{{ title }}</h1>
    <h3>You have clicked {{ clicks }} times!</h3>
    <!-- Add event listeners -->
    <button v-on:click="clicks++">CLICK ME</button>
    <button v-on:click="resetCount()">RESET</button>
    <!-- You can make elements conditionally appear -->
    <p v-if="clicks === 0">CLICK THE BUTTON</p>
    <p v-else-if="clicks % 2 === 0">EVEN!</p>
    <p v-else>ODD!</p>
  </div>
</template>

<script>
// Use JavaScript for any kind of logic
export default {
  name: "HelloWorld",
  props: {
    title: String, // receive props as such
  },
  // any variables to track
  data() {
    return {
      clicks: 0,
    };
  },
  // To add methods/functions
  methods: {
    resetCount() {
      this.clicks = 0;
      alert("Resetting count!");
    },
  },
};
</script>

// style tag for CSS
<style>
.h1-title {
  color: blue;
  text-decoration: underline;
}

#logo {
  max-height: 4rem;
}
</style>