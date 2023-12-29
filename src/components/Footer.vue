<template>
  <footer class="footer">
      <div class="container">
        <div class="footer-box">
          <router-link to="/" class="footer-logo logo">
            <img src="../assets/img/logo.png" alt="Логотип">
          </router-link>
          <div class="footer-nav">
            <ul>
              <li><a href="goods.html">Ресторанам</a></li>
              <li><a href="index.html">Курьерам</a></li>
              <li>Пресс-центр</li>
              <li>Контакты</li>
            </ul>
          </div>
          <div class="footer-social">
            <img src="../assets/img/social/instagram.png" alt="Иконка инстограмм">
            <img src="../assets/img/social/fb.png" alt="Иконка фейсбук">
            <img src="../assets/img/social/vk.png" alt="Иконка вкантакте">
          </div>
        </div>
      </div>
    </footer>
</template>

<script>
export default {

}
</script>

<style scoped>

.footer {
  min-height: 156px;
  display: flex;
  align-items: center;
  padding-top: 60px;
  padding-bottom: 60px;
}

.footer-box {
  height: 100%;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
  gap: 36px;
}

.footer-nav {
  flex-grow: 1;

}

.footer-nav ul {
  display: flex;
  align-items: center;
  list-style: none;
  flex-wrap: wrap;
  padding: 0;
  margin: 0;
  gap: 15px;
}

.footer-nav ul li {
  color: #595959;
  font-size: 18px;
  font-weight: 400;
}

.footer-social {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  gap: 20px;
}
</style>