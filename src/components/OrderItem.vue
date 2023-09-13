<template>
  <div class="item">
    <div class="item__elements">
      <slot class="item__img"></slot>
      <h5 class="item__text">{{ text }}</h5>
    </div>
    <img
      v-if="isDots() === 'true'"
      src="../assets/div.png"
      alt="dots"
      class="item__dots"
    />
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {
    isDots() {
      console.log(this.dots);
      return this.dots;
    },
  },
  props: ["text", "dots"],
};
</script>

<style lang="scss" scoped>
$ffamily: "Lato", sans-serif;
.item {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  gap: 10px;
}
.item__elements {
  display: flex;
  flex-direction: column;
  gap: 20px;
  align-items: center;
}

.item__text {
  max-width: 188px;
  text-align: center;
  color: #fff;
  font-family: $ffamily;
  font-size: 16px;
  font-weight: 400;
}

.item__dots {
  max-width: 110px;
  padding-top: 50px;
  justify-content: center;
  align-items: center;
  padding: 50px 8px 0 8px;
}
</style>
