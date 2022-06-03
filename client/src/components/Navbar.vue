<template>
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
  </div>
</template>

<script>
export default {
  name: "NavigationBar",
  data() {
    return {
      links: ["Главная", "Сеансы", "Отзывы", "Контакты", "Новости", "Обо мне", "Блог"],
    };
  },
};
</script>

<style scoped lang="scss">
.navbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 20px 0 0;
  height: 50px;
}

.nav_logo {
  height: 100%;

  & > img {
    height: 100%;
    width: 100%;
  }
}

.nav_links {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 40px;
}
</style>
