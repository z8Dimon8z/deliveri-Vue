

<template>
   <section class="banner">
        <div class="container">
          <div class="banner-item">
            <h2 class="banner-item--title">Онлайн-сервис<br> доставки еды на дом</h2>
            <p class="banner-item--subtitle">Блюда из любимого ресторана привезет курьер в перчатках, маске и с
              антисептиком</p>
          </div>
        </div>
      </section>

      <section class="products">
        <div class="container">
          <div class="products-header">
            <h3 class="products-header--title">Рестораны</h3>
            <input type="text" class="products-header--search" placeholder="Поиск блюд и ресторанов">
          </div>
          <div class="products-wrapper" id="rest-container">
            <router-link 
             class="products-card"
              v-for="rest in restArray"
              :key="rest.id"
              :to="`/rest?id=${rest.id}`"
            >
              <div class="products-card__image">
                <img :src="getUrl(rest.image)" alt="Картинка ресторана">
              </div>
              <div class="products-card__description">
                <div class="products-card__description-row">
                  <h3 class="products-card__description--title">{{rest.title}}</h3>
                  <div class="products-card__description--badge">{{rest.time}} мин</div>
                </div>

                <div class="products-card__description-row">
                  <div class="products-card__description-info">
                    <div class="products-card__description-info--raiting">
                      <img src="../assets/img/star.svg" alt="Звезда рейтинга">
                      {{rest.raiting}}
                    </div>
                    <div class="products-card__description-info--price">{{rest.price}}</div>
                    <div class="products-card__description-info--group">{{rest.type}}</div>
                  </div>
                </div>
              </div>
            </router-link>

          </div>
        </div>
      </section> 
</template>

<script setup>

 import {restArray} from '../constants/rest'
  const getUrl = (name) => {
    return new URL (`../assets/img/rest/${name}`, import.meta.url)
  }


</script>