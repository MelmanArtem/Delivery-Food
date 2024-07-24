<template>
	<section class="banner">
		<div class="container">
			<div class="banner-item">
				<h2 class="banner-item--title">Онлайн-сервис <br> доставки еды на дом</h2>
				<p class="banner-item--subtitle">Блюда из любимого ресторана привезет <br> курьер в перчатках, маске и с антисептиком</p>
			</div>
		</div>
	</section>
	<section class="products">
		<div class="container">
			<div class="products-header">
				<h3 class="products-header--title"> Рестораны</h3>
				<input type="text" placeholder="Поиск блюд и ресторанов" class="products-header--search">
			</div>
			<div class="products-wrapper" id="rests-container">

				<router-link 
					class="products-card" 
					v-for="rest in store.rests" 
					:key="rest.id"
					:to="`/rest?id=${rest.id}`"
					>
					<div class="products-card-img">
						<img :src="getUrl(rest.image)" alt="image-1">
					</div>
					<div class="products-card-decription">
						<div class="products-card-decription-row">
							<h4 class="products-card-decription-title">{{rest.title}}</h4>
							<div class="products-card-decription-bage">{{rest.time}} мин</div>
						</div>
						<div class="products-card-decription-row">
							<div class="products-card-decription-info">
								<div class="products-card-decription-info-raiting">
									<img src="../assets/img/icons/star.svg" alt="star"> {{rest.rating}}
								</div>
								<div class="products-card-decription-info-price">От {{rest.price}} ₽</div>
								<div class="products-card-decription-info-group">{{rest.type}}</div>
							</div>
						</div>
					</div>
				</router-link>

			</div>
		</div>
	</section>
</template>



<script setup>
	
	import {store} from '../store/index'

	const getUrl = (name) => {
		return new URL(`../assets/img/restotaunt/${name}`, import.meta.url)
	}
</script>