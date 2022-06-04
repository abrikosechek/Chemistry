<template>
  <div class="about">
    <h2>Об RitmStyle</h2>
    <div class="row">
      <div class="text">
        <h4>RitmStyle массаж</h4>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec in purus, sed
          tellus eget mattis nibh quam. Eu ornare nunc, id est. Erat consectetur etiam a
          sit diam in imperdiet amet. Diam nisl, ipsum suscipit amet. Eleifend amet
          habitasse proin quis adipiscing.
        </p>
        <br />
        <p>
          Nisl convallis mauris in consequat. Sit ac vitae posuere maecenas dictumst quam.
          Felis amet diam, non augue massa. Egestas molestie lobortis rhoncus, elit nulla
          nisl. Habitant tortor at tempor
        </p>
      </div>
      <img src="../../public/session_card.png" class="card" />
    </div>
    <div class="row">
      <img src="../../public/session_card.png" class="card" />
      <div class="text">
        <h4>RitmStyle гидротерапия</h4>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Arcu cras quis ac a non
          ut viverra turpis eget. Hendrerit quis pulvinar massa ipsum sem. Donec posuere
          nulla enim non neque etiam. Eros arcu, pulvinar penatibus luctus ridiculus
          sagittis vel nunc hac. Nisi, diam tincidunt dui viverra. Eget quis ultricies sem
          nunc risus senectus luctus ultricies. Enim feugiat pharetra pharetra et.
          Pulvinar arcu at morbi posuere cursus.
        </p>
        <br />
        <p>
          Fermentum est sit enim velit ornare molestie. Ipsum nisi id sed tempor
          elementum. Mi nunc eget pellentesque ipsum. Suspendisse risus a id vel massa
          tincidunt. Hendrerit blandit in augue vel mi quam magna egestas. Fringilla ac
          lacus viverra ullamcorper leo, enim vitae id aliquam. Magna sed tristique tellus
          enim, netus tempor at elit dui. Ullamcorper hendrerit feugiat libero tellus diam
          egestas dui tellus odio.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "aboutPage",
};
</script>

<style lang="scss">
.about {
  margin-top: 150px;
}

.row {
  display: flex;
  justify-content: space-between;
  gap: 85px;
  margin: 100px 0 0;
  min-height: 365px;

  & > * {
    width: 50%;
  }

  @media (max-width: 1130px) {
    justify-content: center;
    margin: 40px 0 0;

    & > .text {
      width: 80%;

      & > h4 {
        margin: 0 0 10px;
        text-align: center;
        font-size: 30px;
      }

      & > p {
        margin: 0px 0;
        text-align: start;
        font-size: 18px;
      }
    }

    & > .card {
      display: none;
      width: 0;
      height: 0;
    }
  }
}

.text {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 10px 40px;

  h4 {
    margin: 0 0 40px;
    text-align: start;
    font-size: 30px;
  }

  p {
    margin: 10px 0;
    text-align: start;
    font-size: 18px;
  }
}

.card {
  border-radius: 20px;
  width: 100%;
  height: auto;
}
</style>
