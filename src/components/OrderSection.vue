<template>
  <div order>
    <h1 class="order__title"></h1>
    <h4 class="order__subtitle"></h4>
    <order-item
      img="item2.png"
      text="Lorem ipsum dolor
        sit amet"
    ></order-item>
  </div>
</template>

<script>
import OrderItem from "../components/OrderItem.vue";
export default {
  components: {
    OrderItem,
  },
};
</script>

<style lang="scss" scoped></style>
