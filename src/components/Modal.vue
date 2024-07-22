<template>
  <div
    class="cart-modal__overlay"
    :class="{ open: isOpen }"
    @click.self="closeModal()"
  >
    <div class="cart-modal">
      <div class="cart-modal__header">
        <h2 class="cart-modal__header_title">Корзина</h2>
        <span class="cart-modal__header_close" @click="closeModal()">
          <img src="../assets/img/icons/close.svg" alt="close" />
        </span>
      </div>

      <div class="cart-modal__body">
        <div class="cart-item">
          <p class="cart-item_title">Ролл угорь стандарт</p>

          <div class="cart-item__controls">
            <div class="cart-item__controls_price">250 ₽</div>

            <button class="btn btn-outline">-</button>
            <div class="cart-item__controls_count">2</div>
            <button class="btn btn-outline">+</button>
          </div>
        </div>

        <div class="cart-item">
          <p class="cart-item_title">Ролл угорь стандарт</p>

          <div class="cart-item__controls">
            <div class="cart-item__controls_price">250 ₽</div>

            <button class="btn btn-outline">-</button>
            <div class="cart-item__controls_count">2</div>
            <button class="btn btn-outline">+</button>
          </div>
        </div>

        <div class="cart-item">
          <p class="cart-item_title">Ролл угорь стандарт</p>

          <div class="cart-item__controls">
            <div class="cart-item__controls_price">250 ₽</div>

            <button class="btn btn-outline">-</button>
            <div class="cart-item__controls_count">2</div>
            <button class="btn btn-outline">+</button>
          </div>
        </div>
      </div>

      <div class="cart-modal__footer">
        <div class="cart-modal__footer_price">1250 ₽</div>
        <div class="cart-modal__footer_controls">
          <button class="btn btn-primery">Оформить заказ</button>
          <button class="btn btn-outline">Отмена</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const { isOpen } = defineProps({ isOpen: Boolean });
const emit = defineEmits(["toggleModal"]);
const closeModal = () => emit("toggleModal");
</script>

<style scoped>
.cart-modal__overlay {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  display: none;
  align-items: center;
  justify-content: center;

  background-color: rgba(0, 0, 0, 0.4);
}

.cart-modal__overlay.open {
  display: flex;
}

.cart-modal {
  width: 100%;
  max-width: 780px;
  padding: 40px 45px;
  border-radius: 5px;
  background: #fff;
}

.cart-modal__header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 48px;
}

.cart-modal__header_title {
  margin: 0;
  color: #000;
  font-size: 36px;
  font-weight: 700;
}

.cart-modal__header_close {
  cursor: pointer;
}

.cart-item {
  padding: 15px 0 10px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 10px;
  border-bottom: 1px solid #d9d9d9;
}

.cart-item_title {
  margin: 0;
  color: #000;
  font-size: 18px;
  line-height: 32px; /* 177.778% */
}

.cart-item__controls {
  display: flex;
  align-items: center;
}

.cart-item__controls button {
  color: #40a9ff;
  font-size: 14px;
  line-height: 22px; /* 157.143% */
  border-radius: 2px;
  border: 1px solid #40a9ff;
  background: #fff;
}

.cart-item__controls_price {
  margin-right: 47px;
  color: #000;
  font-size: 20px;
  font-weight: 700;
  line-height: 32px; /* 160% */
}

.cart-item__controls_count {
  margin: 0 11px;
  color: #000;
  font-size: 16px;
  line-height: 24px; /* 150% */
}

.cart-modal__footer {
  margin-top: 50px;
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  align-items: center;
  justify-content: space-between;
}

.cart-modal__footer_price {
  padding: 15px 20px;
  border-radius: 5px;
  background: #262626;
  color: #fafafa;
  font-size: 20px;
  font-weight: 700;
}

.cart-modal__footer_controls {
  display: flex;
  align-items: center;
  gap: 10px;
}
</style>
