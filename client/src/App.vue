<template>
  <div id="app">
    <Navbar />
    <main>
      <router-view />
    </main>
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";

export default {
  name: "App",
  components: {
    Navbar,
  },
};
</script>

<style lang="scss">
body {
  overflow: overlay;
  margin: 0;
  padding: 40px 0;
  background: linear-gradient(rgb(91, 63, 95), rgb(63, 44, 65));
  background-size: 100% 100%;
  background-repeat: no-repeat;
  min-height: 200vh;

  &::-webkit-scrollbar {
    background-color: rgba(239, 239, 239, 0.9);
    width: 8px;
  }

  &::-webkit-scrollbar-thumb {
    background-color: rgb(107, 107, 107);
    border-radius: 3px;
  }
}

* {
  box-sizing: border-box;
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
  margin: 0;
  padding: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  width: 100%;
  max-width: 1200px;
  margin: 0 auto;

  background-color: white;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

main {
  padding: 20px 0;
}
</style>
