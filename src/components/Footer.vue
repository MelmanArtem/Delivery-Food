<template>
	<footer class="footer">
			<div class="container">
				<div class="footer-box">
					<router-link to="/" class="footer-logo logo">
						<img src="../assets/img/icons/logo.png" alt="logo" />
					</router-link>
					<div class="footer-nav">
						<ul>
							<li>Ресторанам</li>
							<li>Курьерам</li>
							<li>Пресс-центр</li>
							<li>Контакты</li>
						</ul>
					</div>
					<div class="footer-social">
						<a class="" href="https://music.youtube.com/"><img src="../assets/img/social/inst.png" alt="inst" /></a>
						<a class="" href="https://www.youtube.com/"><img src="../assets/img/social/fb.png" alt="fb" /></a>
						<a class="" href="https://vk.com/artem_melman"><img src="../assets/img/social/vk.png" alt="vk" /></a>
					</div>
				</div>
			</div>
		</footer>
</template>

<script>
export default {

}
</script>

<style scoped>
	.footer {
	min-height: 156px;
	display: flex;
	align-items: center;
	padding: 60px 0px;
}
	.footer-box {
	height: 100%;
	display: flex;
	justify-content: space-between;
	align-items: center;
	gap: 36px;
	flex-wrap: wrap;
}
	.footer-nav {
	flex-grow: 1;
}
	.footer-nav ul {
	display: flex;
	align-items: center;
	gap: 15px;
	list-style: none;
	margin: 0;
	padding: 0;
	flex-wrap: wrap;
}
	.footer-nav ul li {
	color: #595959;
	font-size: 18px;
	font-weight: 400;
}
	.footer-social {
	display: flex;
	align-items: center;
	justify-content: flex-end;
	gap: 20px;
}
</style>