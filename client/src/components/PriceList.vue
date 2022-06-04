<template>
  <div class="priceList">
    <h2>Стоимость сеанса</h2>
    <div class="content">
      <div class="list">
        <ul class="titles">
          <li v-for="(product, id) in products" :key="id">{{ product.title }}</li>
        </ul>
        <ul class="prices">
          <li v-for="(product, id) in products" :key="id">{{ product.price }}р.</li>
        </ul>
      </div>
      <div class="card">
        <img src="../../public/coupon.png" alt="coupon" />
        <router-link to="/">Подарочный сертификат</router-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PriceList",
  data() {
    return {
      products: [
        { title: "RitmStyle", price: "1000" },
        { title: "RitmStyle", price: "5500" },
        { title: "RitmStyle", price: "6000" },
        { title: "RitmStyle", price: "13500" },
        { title: "RitmStyle", price: "11500" },
      ],
    };
  },
};
</script>

<style lang="scss">
.priceList {
  margin-top: 150px;
}

.content {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  margin-top: 100px;

  @media (max-width: 950px) {
    margin-top: 20px;
    flex-direction: column;
  }
}

.list {
  display: flex;
  gap: 50px;

  .titles {
    li {
      margin: 30px;

      font-size: 18px;
      list-style-type: none;

      &:before {
        content: "";

        position: relative;
        float: left;
        right: 8px;
        top: 0.35em;
        width: 18px;
        height: 9px;

        background-color: #018abe;
        border-radius: 0 50px;
      }
    }
    @media (max-width: 400px) {
      li:before {
        content: "";

        position: relative;
        float: none;
        right: 0;
        top: 0;
        width: 0;
        height: 0;

        background-color: white;
        border-radius: 0 0;
      }
    }
  }

  .prices {
    li {
      margin: 30px;

      font-size: 18px;
      list-style-type: none;
    }
  }

  @media (max-width: 950px) {
    gap: 20px;
  }

  @media (max-width: 400px) {
    gap: 0;
  }
}

.card {
  display: flex;
  flex-direction: column;
  gap: 30px;
  max-width: 530px;

  background-color: transparent;

  & > img {
    width: 100%;
    height: auto;

    border-radius: 10px;
  }

  & > a {
    font-size: 21px;
    text-align: center;
    text-decoration: underline;
  }

  @media (max-width: 950px) {
    & > img {
      width: 0px;
      height: 0px;
    }
  }
}
</style>
