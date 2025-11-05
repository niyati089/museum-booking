<template>
  <div id="app">
    <nav>
      <h1>{{ appTitle }}</h1>
      <ul>
        <li><a href="#" @click="currentPage = 'home'">Home</a></li>
        <li><a href="#" @click="currentPage = 'about'">About</a></li>
        <li><a href="#" @click="currentPage = 'contact'">Contact</a></li>
      </ul>
    </nav>

    <section v-if="currentPage === 'home'">
      <h2>Welcome to AmuseYou</h2>
      <p>Museum booking for your amusement</p>
    </section>

    <section v-else-if="currentPage === 'about'">
      <h2>About Us</h2>
      <p>This SPA is built using Vue.js by Niyati.</p>
    </section>

    <section v-else>
      <h2>Contact</h2>
      <p>Email us at info@example.com</p>
    </section>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      appTitle: "AmuseYou",
      description: "A simple single page application built with Vue.js.",
      currentPage: "home",
    };
  },
};
</script>

<style>
body {
  font-family: Arial, sans-serif;
  background-color: #f5f8f7;
  margin: 0;
  padding: 0;
}

nav {
  background-color: #4caf50;
  color: white;
  padding: 1em;
  text-align: center;
}

nav ul {
  list-style: none;
  padding: 0;
}

nav li {
  display: inline;
  margin: 0 15px;
}

section {
  padding: 2em;
  text-align: center;
}
</style>

