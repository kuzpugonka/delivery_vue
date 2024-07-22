<template>
  <header class="header">
    <div class="container header__container">
      <div class="header__logo logo">
        <router-link to="/">
          <img src="../assets/img/logo.png" alt="logo" />
        </router-link>
      </div>
      <div class="header__controls">
        <button class="btn btn-primery">
          <img src="../assets/img/icons/user.png" alt="user" />Войти
        </button>
        <button class="btn btn-outline" @click="openModal()">
          <img
            src="../assets/img/icons/shopping-cart.png"
            alt="shopping-cart"
          />Корзина
        </button>
      </div>
    </div>
  </header>
</template>

<script setup>
const emit = defineEmits(["toggleModal"]);
const openModal = () => emit("toggleModal");
</script>

<style scoped>
.header {
  display: flex;
  align-items: center;
  min-height: 124px;
}

.header__container {
  height: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.header__controls {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  gap: 10px;
}
</style>
