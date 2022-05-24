<template>
  <header class="navbar">
    <a class="navbar-logo" href="/home">
      <img src="../assets/logo.png" alt="logo" />
    </a>
    <div class="navbar-links">
      <a href="/home"><p>Мультифильмы</p></a>
      <a href="/home"><p>Для взрослых</p></a>
      <a href="/home"><p>Для детей</p></a>
      <a href="/home"><p>Правообладателям</p></a>
    </div>
  </header>
</template>

<script>
export default {
  name: "Navbar",
};
</script>
<style lang="scss">
.navbar {
  position: sticky;
  top: 0px;
  display: flex;
  justify-content: space-between;
  background: white;

  width: 100%;
  height: 60px;
  box-shadow: 0 10px 10px -10px rgb(0 0 0 / 20%);
}

.navbar__logo {
  height: 100%;

  img {
    height: 100%;
  }
}

.navbar-links {
  & > a {
    & > p {
      &:before {
        width: 10px;
        height: 10px;
        border-radius: 3px;
        margin-right: 10px;
        display: inline-block;
        vertical-align: middle;
        background: #ffba00;
        content: "";
      }
    }
  }
}
</style>
