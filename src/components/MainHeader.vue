<template>
  <div class="header">
    <div class="wrapper">
      <div class="header__inner">
        <a href="#">
          <img
            class="header__logo"
            src="../assets/logo.png"
            alt="LoremIpsum.net"
        /></a>
        <i class="fa-solid fa-bars header__menu"></i>
        <ul class="header__links">
          <a class="header__link" href="#">Бизнес</a>
          <a class="header__link" href="#">О нас</a>
          <a class="header__link" href="#">Цены</a>
          <a class="header__link" href="#">Оформить заказ</a>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
$color: #3e9cdc;
.header {
  width: 100%;
  background-color: rgba(16, 16, 29, 0.9);
  position: fixed;
}

.header__inner {
  height: 100px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}
.header__logo {
  width: 247px;
  height: 23px;
}
.header__links {
  display: flex;
  flex-direction: row;
  gap: 60px;
}

.header__menu {
  display: none;
  color: #fff;
}

.header__link {
  color: #fff;
  font-family: "Lato", sans-serif;
  font-size: 13px;
  font-weight: 600;
  text-transform: uppercase;
  &:hover {
    color: $color;
  }
}

@media (max-width: 770px) {
  .header__logo {
    width: 180px;
    height: 15px;
  }
  .header__links {
    display: flex;
    flex-direction: row;
    gap: 30px;
  }
  .header__link {
    font-size: 11px;
  }
}

@media (max-width: 550px) {
  .header__links {
    display: none;
  }

  .header__menu {
    display: block;
  }
}
</style>
