<template>
  <div class="footer">
    <h4 class="footer__item">© 2018 «LoremIpsum.net» Все права защищены.</h4>
    <h4>|</h4>
    <div class="footer__item">
      <img src="../assets/qiwi.png" alt="" />Qiwi wallet
    </div>
    <div class="footer__item">
      <img src="../assets/yandex.png" alt="" />Yandex wallet
    </div>
    <div class="footer__item">
      <img src="../assets/web.png" alt="" />Web money
    </div>
    <h4>|</h4>
    <a class="footer__item" href="#"
      ><img src="../assets/email.png" />info@ipsum228.com</a
    >
    <a class="footer__item" href="#"
      ><img src="../assets/vk.png" />Мы вконтакте</a
    >
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
$ffamily: "Lato", sans-serif;
.footer {
  color: #fff;
  background: #3d4050;
  padding: 30px 0;
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 40px;
  justify-content: center;
}
.footer__item {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 10px;
  color: #fff;
  font-size: 13px;
  font-weight: 400;
  font-family: $ffamily;
}
</style>
