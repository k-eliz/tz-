<template>
  <div class="intro">
    <div class="wrapper">
      <div class="intro__inner">
        <h1 class="intro__title">
          <span class="intro__title_blue">Lorem ipsum</span> dolor sit amet
          consectetur <span class="intro__title_blue">adipiscing</span>
        </h1>
        <ul class="intro__list">
          <h3 class="intro__text">
            At vero eos et accusamus et iusto odio dignissimos ducimus!
          </h3>
          <li class="intro__item">Totam rem aperiam eaque ipsa</li>
          <li class="intro__item">
            Sit voluptatem accusantium doloremque laudantium
          </li>
          <li class="intro__item">
            Sed ut perspiciatis, unde omnis iste natus error
          </li>
        </ul>
        <div class="intro__buttons">
          <my-button class="intro__btn_blue">Заказать</my-button>
          <my-button class="intro__btn_white">Подробнее</my-button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import MyButton from "../components/UI/MyButton.vue";
export default {
  components: {
    MyButton,
  },
};
</script>

<style lang="scss" scoped>
$color: #3e9cdc;
$ffamily: "Lato", sans-serif;
.intro {
  background: url("../assets/bg.jpg") center no-repeat;
  background-size: cover;
  height: 100vh;
  padding-top: 203px;
}

.intro__inner {
  display: flex;
  flex-direction: column;
  gap: 80px;
}
.intro__title {
  color: #000;
  font-family: $ffamily;
  font-size: 48px;
  font-weight: 700;
  text-transform: uppercase;
  max-width: 780px;
  line-height: normal;
  .intro__title_blue {
    color: $color;
  }
}

.intro__list {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.intro__item {
  &:before {
    content: "- ";
  }
  color: #000;
  font-family: $ffamily;
  font-size: 20px;
  font-weight: 400;
}

.intro__text {
  color: #000;
  font-family: $ffamily;
  font-size: 20px;
  font-weight: 700;
}

.intro__buttons {
  display: flex;
  flex-direction: row;
  gap: 30px;

  .intro__btn_blue {
    border-color: #fff;
    background-color: $color;
    color: #fff;
    text-align: center;
    font-family: $ffamily;
    font-size: 16px;
    font-weight: 400;
    text-transform: uppercase;
  }

  .intro__btn_white {
    border-color: #6f6d7b;
    background-color: #fff;
    color: #2a2b30;
    text-align: center;
    font-family: $ffamily;
    font-size: 16px;
    font-weight: 400;
    text-transform: uppercase;
  }
}

@media (max-width: 1400px) {
  .intro {
    width: 100 vw;
  }
}
@media (max-width: 770px) {
  .intro__title {
    font-size: 36px;
  }
  .intro__item {
    font-size: 16px;
  }

  .intro__text {
    font-size: 16px;
  }
}
</style>
