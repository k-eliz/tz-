<template>
  <div class="order">
    <div class="wrapper">
      <div class="order__inner">
        <h1 class="order__title">
          Оформление <span class="order__title_blue">Заказа</span>
        </h1>
        <h4 class="order__subtitle">
          Перед заполнением формы ознакомьтесь с нашей схемой работы!
        </h4>
        <div class="order__items">
          <order-item
            text="Lorem ipsum dolorI
        sit amet"
            dots="true"
            ><img class="order__img" src="../assets/item1.png" alt="item"
          /></order-item>
          <order-item text="Сonsecteturadipiscing elit" dots="true"
            ><img class="order__img" src="../assets/item2.png" alt="item"
          /></order-item>
          <order-item text="Sed do eiusmod tempor" dots="true"
            ><img class="order__img" src="../assets/item3.png" alt="item"
          /></order-item>
          <order-item
            text="Esse cillum dolore
                eu fugiat"
            dots="true"
            ><img class="order__img" src="../assets/item4.png" alt="item"
          /></order-item>
          <order-item
            text="Excepteur sint occaecat cupidatat non proident"
            dots="false"
            ><img class="order__img" src="../assets/item5.png" alt="item"
          /></order-item>
        </div>
        <div class="order__inputs">
          <select class="order__select" name="select">
            <div class="placeholder" data-text="Выберите тип системы"></div>
            <option class="order__option" value="1">Sed ut perspiciatis</option>
            <option class="order__option" value="2">Nemo enim ipsam</option>
            <option class="order__option" value="3">Et harum quidem</option>
            <option class="order__option" value="4">Temporibus autem</option>
            <option class="order__option" value="5">Itaque earum rerum</option>
          </select>
          <input class="order__input" type="text" placeholder="Ваш e-mail" />
          <input class="order__input" type="text" placeholder="Ваше имя" />
          <div class="order__range">
            <h6 class="order__range_text">
              Sed ut perspiciatis, unde omnis iste natus
            </h6>
            <input
              class="slider"
              type="range"
              min="0"
              max="100"
              step="1"
              value="75"
              id="myRange"
            />
          </div>

          <my-button class="order__btn_file"
            ><img src="../assets/btn.png" alt="" />Прикрепить файл</my-button
          >
          <my-button class="order__btn_send">Отправить</my-button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import OrderItem from "../components/OrderItem.vue";
import MyButton from "./UI/MyButton.vue";
export default {
  data() {
    return {
      range: document.querySelector(".slider"),
    };
  },
  methods: {
    funcRange() {
      this.range.addEventListener(
        "change",
        function () {
          /* После отжатия кнопки мышки с ползунка */
          console.log(this.value);
        },
        false
      );

      this.range.addEventListener(
        "input",
        function () {
          /* Во время движения ползунка */
          console.log(this.value);
        },
        false
      );
    },
  },
  components: {
    OrderItem,
    MyButton,
  },
};
</script>

<style lang="scss" scoped>
$color: #3e9cdc;
$ffamily: "Lato", sans-serif;
.order {
  background: url("../assets/sectionBG.jpg") center no-repeat;
  background-size: cover;
  height: 100vh;
}

.order__title {
  color: #fff;
  font-family: $ffamily;
  font-size: 36px;
  font-style: normal;
  font-weight: 800;
  line-height: normal;
  text-transform: uppercase;
  padding-top: 170px;
}

.order__inner {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 30px;
}

.order__title_blue {
  color: $color;
}
.order__subtitle {
  color: #bbb;
  font-family: $ffamily;
  font-size: 18px;
  font-weight: 400;
}

.order__img {
  width: 100px;
}

.order__items {
  width: 100%;
  display: flex;
  flex-direction: row;
  padding-top: 50px;
}

.order__inputs {
  width: 100%;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-column-gap: 30px;
  row-gap: 30px;
}
.order__select {
  padding: 10px;
  border-radius: 3px;
  border: 1px solid #fff;
  font-size: 18px;
  font-weight: 400;
  font-family: $ffamily;
  background: rgba(255, 255, 255, 0.85);
  &:focus {
    background: rgba(61, 64, 80, 0.85);
    border: none;
  }
}

.order__option {
  background: rgba(39, 39, 51, 0.9);
  color: #fff;
  font-size: 18px;
  font-weight: 400;
  font-family: $ffamily;
  &:hover {
    color: $color;
    background-color: none;
  }
}

.order__input {
  color: rgba(39, 39, 51, 1);
  font-family: $ffamily;
  padding: 10px;
  border-radius: 3px;
  border: 1px solid #fff;
  background: rgba(255, 255, 255, 0.85);
  font-size: 18px;
  font-weight: 400;
}

.order__range_text {
  padding-bottom: 20px;
  color: #fff;
  font-family: $ffamily;
  font-size: 18px;
  font-weight: 400;
}

.order__range {
  grid-row-start: 2;
  grid-column-start: 1;
  grid-column-end: 3;
}

.slider {
  -webkit-appearance: none;
  width: 100%;
  height: 6px;
  border-radius: 5px;
  background: #d3d3d3;
  outline: none;
  opacity: 1;
  -webkit-transition: 0.2s;
  transition: opacity 0.2s;
}

.slider::-webkit-slider-thumb {
  -webkit-appearance: none;
  appearance: none;
  width: 25px;
  height: 25px;
  border-radius: 50%;
  border: 3px solid rgba(40, 102, 144, 1);
  background: $color;
  cursor: pointer;
}

.slider::-moz-range-thumb {
  width: 25px;
  height: 25px;
  border-radius: 50%;
  border: 3px solid rgba(40, 102, 144, 1);
  border-color: #272733;
  background: $color;
  cursor: pointer;
}
.order__btn_file {
  color: #272733;
  font-family: $ffamily;
  font-size: 15px;
  font-weight: 600;
  text-transform: uppercase;
  width: 100%;
}
.order__btn_send {
  color: #fff;
  font-family: $ffamily;
  background: $color;
  font-size: 15px;
  font-weight: 600;
  text-transform: uppercase;
  width: 100%;
  grid-row-start: 3;
  grid-column-start: 2;
  grid-column-end: 3;
}
</style>
