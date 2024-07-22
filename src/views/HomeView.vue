<template>
  <section class="hero">
    <div class="container hero-container">
      <h2 class="hero__title">Онлайн-сервис <br />доставки еды на&nbsp;дом</h2>
      <p class="hero__subtitle">
        Блюда из любимого ресторана привезет курьер в перчатках, маске и с
        антисептиком
      </p>
    </div>
  </section>

  <section class="products">
    <div class="container">
      <div class="products__header">
        <h3 class="products__header-title">Рестораны</h3>
        <input
          class="products__header-search"
          type="text"
          placeholder="Поиск блюд и ресторанов"
        />
      </div>

      <div class="products__wrapper" id="rects-container">
        <router-link
          class="products-cart"
          v-for="rest in store.rests"
          :key="rest.id"
          :to="`/rest?id=${rest.id}`"
        >
          <div class="products-cart__img">
            <img :src="getUrl(rest.image)" alt="`{{ rest.title }}`" />
          </div>
          <div class="products-cart__desc">
            <div class="products-cart__desc-row">
              <h4 class="products-cart__desc_title">{{ rest.title }}</h4>
              <div class="products-cart__desc_badge">{{ rest.time }} мин</div>
            </div>

            <div class="products-cart__desc-row">
              <div class="products-cart__desc-info">
                <div class="products-cart__desc-info_raiting">
                  <img src="../assets/img/star.svg" alt="star" />
                  {{ rest.reiting }}
                </div>
                <div class="products-cart__desc-info_price">
                  От {{ rest.price }} ₽
                </div>
                <div class="products-cart__desc-info_group">
                  {{ rest.type }}
                </div>
              </div>
            </div>
          </div>
        </router-link>
      </div>
    </div>
  </section>
</template>

<script setup>
import { store } from "../store/index";
import { restArray } from "../constants/rests";
const getUrl = (name) => {
  return new URL(`../assets/img/restorans/${name}`, import.meta.url);
};
</script>
