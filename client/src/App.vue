<template>
  <div id="app">
    <!--    <NavigationBar /> -->
    <router-view />
    <FooterBar />
  </div>
</template>

<script>
//import NavigationBar from "./components/Navbar.vue";
import FooterBar from "./components/FooterBar.vue";

export default {
  name: "App",
  title: "main",
  components: {
    //    NavigationBar,
    FooterBar,
  },
  data() {
    return {};
  },
};
</script>

<style lang="scss">
$accent: #018abe;

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: white;

  width: 100%;

  @media (min-width: 1200px) {
    max-width: 1200px;
  }

  margin: 0 auto;
}

body {
  margin: 0;
  background-color: #162831;
}

.bg--accent {
  background-color: $accent;
}

* {
  box-sizing: border-box;

  &::-webkit-scrollbar {
    width: 6px;
    height: 8px;
  }

  &::-webkit-scrollbar-thumb {
    background-color: $accent;
    border-radius: 2px;
  }
}

h1,
h2,
h3,
h4,
h5,
h6,
p,
a,
span,
label {
  position: relative;
  margin: 0;
  padding: 0;

  color: white;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  text-align: center;
  font-family: sans;
}

h1 {
  font-size: 64px;
  font-weight: 600;
  max-width: 600px;
}

h2 {
  font-size: 42px;
}

h3 {
  font-size: 26px;
}

h4 {
  font-size: 24px;
}

p,
a {
  font-size: 14px;
  font-weight: 200;
  text-decoration: none;
}

button {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 36px;
  padding: 0 14px;

  border-radius: 3px;
  border: none;

  cursor: pointer;
  color: white;

  &.bg--white {
    color: $accent;
  }
}
</style>
