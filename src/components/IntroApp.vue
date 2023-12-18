<template>
	<section class="intro">
		<div class="intro__content">
			<h2 class="intro__title">Смартфоны</h2>
			<nav class="intro__nav">
				<div class="intro__nav-title">Отобразить товары:</div>
				<ul class="intro__nav-amount">
					<li class="intro__nav-count"
					v-for="i in 5">{{ i + 1 }}</li>
				</ul>
			</nav>
		</div>
		<div class="intro__content">
			<div class="intro__checkbox">
				<input class="intro__checkbox-input" type="checkbox" id="checkbox">
				<label class="intro__checkbox-label" for="checkbox">Показать различия</label>
			</div>
			<div class="intro__inner">
				<div class="intro__item">
					<div class="intro__item-wrapper">
						<img class="intro__item-img" src="../assets/images/apple-12.jpg" alt="phone">
						<button class="intro__item-btn">
							<img src="../assets/images/arrow-down.svg" alt="arrow">
						</button>
					</div>
					<div class="intro__item-name">Apple iPhone 12</div>
				</div>
				<div class="intro__item">
					<div class="intro__item-wrapper">
						<img class="intro__item-img" src="../assets/images/xiaomi-11.jpg" alt="phone">
						<button class="intro__item-btn">
							<img src="../assets/images/arrow-down.svg" alt="arrow">
						</button>
					</div>
					<div class="intro__item-name">Xiaomi Mi 11 Lite</div>
				</div>
				<div class="intro__item">
					<div class="intro__item-wrapper">
						<img class="intro__item-img" src="../assets/images/samsung-72.jpg" alt="phone">
						<button class="intro__item-btn">
							<img src="../assets/images/arrow-down.svg" alt="arrow">
						</button>
					</div>
					<div class="intro__item-name">Samsung Galaxy A72</div>
				</div>

				<div class="intro__item">
					<div class="intro__item-wrapper">
						<img class="intro__item-img" src="../assets/images/samsung-72.jpg" alt="phone">
						<button class="intro__item-btn">
							<img src="../assets/images/arrow-down.svg" alt="arrow">
						</button>
					</div>
					<div class="intro__item-name">Samsung Galaxy A72</div>
				</div>
				<div class="intro__item">
					<div class="intro__item-wrapper">
						<img class="intro__item-img" src="../assets/images/xiaomi-11.jpg" alt="phone">
						<button class="intro__item-btn">
							<img src="../assets/images/arrow-down.svg" alt="arrow">
						</button>
					</div>
					<div class="intro__item-name">Xiaomi Mi 11 Lite</div>
				</div>
				<div class="intro__item">
					<div class="intro__item-wrapper">
						<img class="intro__item-img" src="../assets/images/apple-12.jpg" alt="phone">
						<button class="intro__item-btn">
							<img src="../assets/images/arrow-down.svg" alt="arrow">
						</button>
					</div>
					<div class="intro__item-name">Apple iPhone 12</div>
				</div>


			</div>
		</div>
	</section>
</template>

<script lang="ts">
	import { defineComponent } from 'vue';

	export default defineComponent ({
		name: 'IntroApp'
	});
</script>

<style lang="scss" scoped>

</style>