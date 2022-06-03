<template>
  <div class="mainPage">
    <div class="intro">
      <h3>Укрепление здоровья</h3>
      <h1>Акватерапия RitmStyle</h1>
    </div>
    <RitmSess />
    <AboutPage />
    <PriceList />
  </div>
</template>

<script>
import RitmSess from "./RitmSess";
import AboutPage from "./aboutPage.vue";
import PriceList from "./PriceList.vue";

export default {
  name: "HomePage",
  components: { RitmSess, AboutPage, PriceList },
};
</script>

<style scoped lang="scss">
.intro {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 60px;
  width: 100%;
  height: 600px;
  margin: 50px 0 0;

  background: url("../../public/mp_intro.png");
  background-size: auto 100%;
  background-position: center;
  border-radius: 14px;
}
</style>
