<template>
  <button class="button">
    <slot></slot>
  </button>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.button {
  width: 183px;
  display: flex;
  padding: 15px 10px;
  justify-content: center;
  align-items: center;
  gap: 10px;
  border-radius: 4px;
  border: 1px solid;
}

@media (max-width: 770px) {
  .button {
    width: 150px;
  }
}
@media (max-width: 650px) {
  .button {
    width: 135px;
  }
}
@media (max-width: 540px) {
  .button {
    height: 50px;
  }
}
</style>
