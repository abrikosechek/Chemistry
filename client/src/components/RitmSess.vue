<template>
  <div class="sessions">
    <h2>Сеансы RitmStyle</h2>

    <div class="session_cards">
      <button
        class="session_card"
        :class="session.class"
        v-for="(session, id) in sessions"
        :key="id"
      >
        <p>
          {{ session.title }}
        </p>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "RitmSess",
  data() {
    return {
      sessions: [
        { title: "Стандартный RitmStyle", class: "card-1" },
        { title: "RitmStyle для пар", class: "card-2" },
        { title: "RitmStyle с полным погружением под воду", class: "card-3" },
        { title: "RitmStyle для беременных", class: "card-4" },
        { title: "RitmStyle + красочная подводная фотосессия", class: "card-5" },
      ],
    };
  },
};
</script>

<style lang="scss">
.sessions {
  margin-top: 150px;
}

.session_cards {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(2, 260px);
  gap: 25px;
  margin-top: 100px;
  width: 100%;

  @media (max-width: 1230px) {
    max-width: 800px;
    margin: 100px auto 0;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(3, 260px);
  }

  @media (max-width: 830px) {
    justify-content: center;
    grid-template-columns: repeat(1, 90%);
    grid-template-rows: repeat(5, 1fr);
  }
}

.session_card {
  display: flex;
  align-items: flex-end;
  justify-content: flex-start;
  padding: 10% 40px;
  width: 100%;
  height: 100%;

  background-image: url("../../public/session_card.png");
  background-position: center;
  background-size: auto 100%;
  border-radius: 10px;

  @media (max-width: 830px) {
    height: 500px;
  }

  @media (max-width: 600px) {
    height: 400px;
  }

  @media (max-width: 500px) {
    height: 300px;
  }

  & > p {
    font-size: 24px;
    font-family: sans;
    text-align: start;
  }
}

@media (min-width: 1231px) {
  .card-1 {
    grid-column-start: 1;
    grid-column-end: 1;
    grid-row-start: 1;
    grid-row-end: 3;

    background-position: 40% center;
  }

  .card-2 {
    grid-column: 2;
    grid-row: 1;
  }

  .card-3 {
    grid-column: 3;
    grid-row: 1;
  }

  .card-4 {
    grid-column: 2;
    grid-row: 2;
  }

  .card-5 {
    grid-column: 3;
    grid-row: 2;
  }
}
</style>
