<script setup>
import Footer from "@/components/Footer.vue";
import Header from "@/components/Header.vue";
import Modal from "@/components/Modal.vue";
import { store } from "./store/index";

</script>

<template>
  <div class="page-wrapper">
    <Header @toggleModal="store.toggleModal(true)"></Header>

    <main class="main">
      <RouterView />
    </main>

    <Modal :isOpen="store.isOpen" @toggleModal="store.toggleModal(false)" />

    <Footer></Footer>
  </div>
</template>

<style scoped></style>
