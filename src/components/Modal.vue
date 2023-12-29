<template>
  <div class="cart-modal__overlay" :class="{open: isOpen}" @click.self="closeModal()">
      <div class="cart-modal">
        <div class="cart-modal__header">
          <h2 class="cart-modal__header--title">Корзина</h2>
          <span class="cart-modal__header--close">
            <img src="../assets/img/icons/close.svg" @click="closeModal()" alt="закрыть">
          </span>
        </div>
        <div class="cart-modal__body">
          <div class="cart-item">
              <p class="cart-item__title">Ролл угорь стандарт</p>
            <div class="cart-item__controls">
              <div class="cart-item__controls--price">250 ₽</div>
              <button class="btn btn-outline">-</button>
              <div class="cart-item__controls--count">1</div>
              <button class="btn btn-outline">+</button>
            </div>
          </div>

          <div class="cart-item">
              <p class="cart-item__title">Ролл угорь стандарт</p>
            <div class="cart-item__controls">
              <div class="cart-item__controls--price">250 ₽</div>
              <button class="btn btn-outline">-</button>
              <div class="cart-item__controls--count">1</div>
              <button class="btn btn-outline">+</button>
            </div>
          </div>

          <div class="cart-item">
              <p class="cart-item__title">Ролл угорь стандарт</p>
            <div class="cart-item__controls">
              <div class="cart-item__controls--price">250 ₽</div>
              <button class="btn btn-outline">-</button>
              <div class="cart-item__controls--count">1</div>
              <button class="btn btn-outline">+</button>
            </div>
          </div>
        </div>
        <div class="cart-modal__footer">
          <div class="cart-modal__footer--price">1250 ₽</div>
          <div class="cart-modal__footer--controls">
            <button class="btn btn-pramary">
              Оформить заказ
            </button>
            <button class="btn btn-outline">
              Отмена
            </button>
          </div>
        </div>
      </div>
    </div>
</template>

<script setup>
    const {isOpen} = defineProps({
      isOpen: Boolean
    })
    const emit = defineEmits(['toggleModal'])
  const closeModal = () => emit('toggleModal')
</script>

<style scoped>

.cart-modal__overlay {
  display: none;
  background-color: rgba(0, 0, 0, 0.40);
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  align-items: center;
  justify-content: center;
}

.cart-modal__overlay.open{
  display: flex;
}

.cart-modal {
  padding: 40px 45px;
  width: 100%;
  max-width: 780px;
  border-radius: 5px;
  background-color: #FFF;
}

.cart-modal__header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 48px;
}

.cart-modal__header--title {
  color: #000;
  font-size: 36px;
  font-weight: 700;
  margin: 0;
}

.cart-modal__header--close {
  cursor: pointer;
}


.cart-modal__footer {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 15px;
  margin-top: 50px;
}

.cart-modal__footer--price {
  padding: 15px 20px;
  color: #FAFAFA;
  font-size: 20px;
  font-weight: 700;
  border-radius: 5px;
  background-color: #262626;
}

.cart-modal__footer--controls {
  display: flex;
  align-items: center;
  gap: 10px;
  flex-wrap: wrap;
}

</style>
