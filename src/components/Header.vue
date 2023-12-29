<template>
  <header class="header">
      <div class="container">
        <div class="header-box">
          <router-link to="/" class="header-logo logo">
            <img src="../assets/img/logo.png" alt="Логотип">
          </router-link>
          <div class="header-controls">
            <button class="btn btn-pramary">
              <img src="../assets/img/icons/user.png" alt="Иконка пользователя">
              Войти
            </button>
            <button class="btn btn-outline" @click="openModal()">
              <img src="../assets/img/icons/shopping-cart.png" alt="Иконка корзины">
              Корзина
            </button>
          </div>
        </div>
      </div>
    </header>
</template>

<script setup>
  const emit = defineEmits(['toggleModal'])
  const openModal = () => emit('toggleModal')
  
</script>

<style scoped>

.header {
  min-height: 124px;
  display: flex;
  align-items: center;
}

.header-box {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.header-controls {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  gap: 10px;
}
</style>