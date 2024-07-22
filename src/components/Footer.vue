<template>
  <footer class="footer">
    <div class="container footer-container">
      <div class="footer__logo logo">
        <router-link to="/">
          <img src="../assets/img/logo.png" alt="logo" />
        </router-link>
      </div>

      <div class="footer__nav">
        <ul>
          <li><router-link to="/rest">Ресторанам</router-link></li>
          <li><router-link to="/rest">Курьерам</router-link></li>
          <li><router-link to="/rest">Пресс-центр</router-link></li>
          <li><router-link to="/rest">Контакты</router-link></li>
        </ul>
      </div>

      <div class="footer__social">
        <img src="../assets/img/social/inst.png" alt="inst" />
        <img src="../assets/img/social/fb.png" alt="fb" />
        <img src="../assets/img/social/vk.png" alt="vk" />
      </div>
    </div>
  </footer>
</template>

<script>
export default {};
</script>

<style scoped>
.footer {
  padding: 60px 0;
  display: flex;
  align-items: center;
  min-height: 156px;
}

.footer-container {
  height: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
  gap: 36px;
}

.footer__nav {
  flex-grow: 1;
}

.footer__nav ul {
  margin: 0;
  padding: 0;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 15px;
  list-style: none;
}

.footer__nav ul li {
  color: #595959;
  font-weight: 400;
  font-size: 18px;
}

.footer__nav a {
  text-decoration: none;
  cursor: pointer;
}

.footer__social {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  gap: 20px;
}
</style>
