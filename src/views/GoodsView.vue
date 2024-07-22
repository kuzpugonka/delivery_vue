<template>
  <section class="products">
    <div class="container">
      <div class="products__header">
        <h4 class="products__header-title">Тануки</h4>
        <div class="products-cart__desc-info">
          <div class="products-cart__desc-info_raiting">
            <img src="../assets/img/star.svg" alt="star" />
            4.5
          </div>
          <div class="products-cart__desc-info_price">От 900 ₽</div>
          <div class="products-cart__desc-info_group">Пицца и суши</div>
        </div>
      </div>

      <div class="products__wrapper" id="goods-container">
        <!-- origin -->
        <div class="products-cart" v-for="good in goodsArray" :key="good.id">
          <div class="products-cart__img">
            <img :src="getUrl(good.image)" alt="good" />
          </div>
          <div class="products-cart__desc">
            <div class="products-cart__desc-row">
              <h5 class="products-cart__desc_name">{{ good.title }}</h5>
            </div>

            <div class="products-cart__desc-row">
              <p class="products-cart__desc_text">
                {{ good.text }}
              </p>
            </div>

            <div class="products-cart__desc-row">
              <div class="products-cart__desc-controls">
                <button class="btn btn-primery">
                  <img
                    src="../assets/img/icons/shopping-cart.svg"
                    alt="user"
                  />В корзину
                </button>
                <span class="products-cart__desc-controls_price">{{ good.price }} ₽</span>
              </div>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
import { goodsArray } from "@/constants/goods";
const getUrl = (name) => {
  return new URL(`../assets/img/goods/${name}`, import.meta.url);
};
</script>
