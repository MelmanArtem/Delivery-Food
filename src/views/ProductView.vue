<template>
  <section class="products">
    <div class="container">
      <div class="products-wrapper" id="products-container">

        <router-link 
				class="products-card" 
				v-for="rest in prodArray" 
				:key="rest.id"
				:to="`/rest?id=${rest.id}`"
		  >
          <div class="products-card-img">
            <img :src="getUrl(rest.image)" alt="prod-1" />
          </div>
          <div class="products-card-decription">
            <div class="products-card-decription-row">
              <h5 class="products-card-decription--name">
                {{rest.title}}
              </h5>
            </div>
            <div class="products-card-decription-row">
              <p class="products-card-decription--text">
                {{rest.description}}
              </p>
            </div>
            <div class="products-card-decription-row">
              <div class="products-card-decription--controls">
                <button class="btn btn-primary">
                  В корзину
                  <img
                    src="../assets/img/icons/shopping-cart.svg"
                    alt="shopping-cart-white"
                  />
                </button>
                <span class="products-card-decription-controls--price">
                  {{rest.price}} ₽
                </span>
              </div>
            </div>
          </div>
        </router-link>
      </div>
    </div>
  </section>
</template>

<script setup>

	import {prodArray} from '../constants/prod'

	const getUrl = (name) => {
		return new URL(`../assets/img/products/${name}`, import.meta.url)
	}
</script>