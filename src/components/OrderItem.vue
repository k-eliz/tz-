<template>
  <div class="item">
    <img :src="source" alt="item" />
    <h5>{{ text }}</h5>
  </div>
</template>

<script setup>
import { computed, defineProps } from "vue";

const props = defineProps(["text", "img"]);

const source = computed(() => {
  return new URL(`../assets/${props.img}`, import.meta.url).href;
});
// export default {
//   data: () => {
//     return {
//       source: "",
//     };
//   },
//   props: {
//     text: {
//       type: String,
//       required: true,
//     },
//     img: {
//       type: String,
//       required: true,
//     },
//   },
//   // computed: {
//   //   imgSrc() {
//   //     console.log(this.props);
//   //     if (this.props?.img) {
//   //       return new URL(`../assets/${this.props.img}`, import.meta.url).href;
//   //     }
//   //     return "";
//   //   },
//   // },
//   watch:{
//     img(){

//     }
//   }
// };
</script>

<style lang="scss" scoped>
.item {
  display: flex;
  flex-direction: column;
  gap: 20px;
}
</style>
