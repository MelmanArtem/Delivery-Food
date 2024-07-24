<template>
	<header class="header">
		<div class="container">
			<div class="header-box">
				<router-link to="/" class="header-logo logo">
					<img src="../assets/img/icons/logo.png" alt="logo" />
				</router-link>
				<div class="header-controls">
					<button class="btn btn-primary">
						<img src="../assets/img/icons/user.png" alt="user" />Войти
					</button>
					<button class="btn btn-outline" @click="openModal()">
						<img src="../assets/img/icons/shopping-cart.png" alt="cart" />Корзина
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
	justify-content: space-between;
	align-items: center;
}
	.header-controls {
	display: flex;
	align-items: center;
	gap: 8px;
	justify-content: flex-end;
}
</style>