<template>
  <footer>
    <p>© 2018-2022 RitmStyle</p>
    <p>Сделано d-e-n.info</p>
  </footer>
</template>

<script>
export default {};
</script>

<style lang="scss">
footer {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-top: 70px;
  padding: 20px 0 20px;

  @media (max-width: 1200px) {
    background-color: #233f4d;
    padding: 20px 20px 10px;
  }

  @media (max-width: 860px) {
    padding: 10px 10% 10px;
  }
}
</style>
