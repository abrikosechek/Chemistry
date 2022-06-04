<template>
  <div :class="{ hidden: menu_hidden }" class="menu">
    <router-link to="/main">{{ links[0] }}</router-link>
    <router-link to="/main">{{ links[1] }}</router-link>
    <router-link to="/main">{{ links[2] }}</router-link>
    <router-link to="/main">{{ links[3] }}</router-link>
    <router-link to="/main">{{ links[4] }}</router-link>
    <router-link to="/main">{{ links[5] }}</router-link>
    <router-link to="/main">{{ links[6] }}</router-link>
    <button
      class="menu_toggler"
      style="color: black"
      v-on:click="menu_hidden = !menu_hidden"
    >
      X
    </button>
  </div>
  <div class="navbar">
    <router-link to="/main" class="nav_logo">
      <img src="../../public/logo.svg" />
    </router-link>
    <div class="nav_links">
      <router-link to="/main">{{ links[0] }}</router-link>
      <router-link to="/main">{{ links[1] }}</router-link>
      <router-link to="/main">{{ links[2] }}</router-link>
      <router-link to="/main">{{ links[3] }}</router-link>
      <router-link to="/main">{{ links[4] }}</router-link>
      <router-link to="/main">{{ links[5] }}</router-link>
      <router-link to="/main">{{ links[6] }}</router-link>
    </div>
    <button class="bg--accent">Записаться на сеанс</button>
    <button
      class="menu_toggler"
      style="color: black"
      v-on:click="menu_hidden = !menu_hidden"
    >
      X
    </button>
  </div>
</template>

<script>
export default {
  name: "NavigationBar",
  data() {
    return {
      menu_hidden: true,
      links: ["Главная", "Сеансы", "Отзывы", "Контакты", "Новости", "Обо мне", "Блог"],
    };
  },
};
</script>

<style scoped lang="scss">
.hidden {
  display: none;
}

.menu {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 30;

  background-color: whitesmoke;
  & > a {
    color: black;
  }
}

.navbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  margin: 20px 0 0;
  height: 50px;

  .nav_links {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 40px;
  }

  @media (max-width: 1205px) {
    width: auto;
    margin: 10px 0;
    padding: 0 20px;
  }

  @media (max-width: 910px) {
    width: auto;
    margin: 10px 0;
    padding: 0 20px;

    & > .nav_links {
      display: none;
    }
  }
}

.nav_logo {
  height: 100%;

  & > img {
    height: 100%;
    width: 100%;
  }
}

@media (min-width: 910px) {
  .menu_toggler {
    display: none;
  }
}
</style>
