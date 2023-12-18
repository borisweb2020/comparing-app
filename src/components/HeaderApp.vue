<template>
	<header class="header">
		<div class="container">
			<div class="header__inner">
				<a class="header__link" href="#">Каталог</a>
				<nav class="header__nav">
					<h3 class="header__nav-title">Сравнение</h3>
					<ul class="header__nav-menu">
						<li class="header__nav-item">
							<a class="header__nav-link" href="#">Личный кабинет</a>
						</li>
						<li class="header__nav-item">
							<a class="header__nav-user" href="#">
								<img class="header__nav-icon" src="../assets/images/user.svg" alt="icon">
							</a>
						</li>
					</ul>
				</nav>
			</div>
		</div>
	</header>
</template>

<script lang="ts">
	import { defineComponent } from 'vue';

	export default defineComponent ({
		name: 'HeaderApp'
	});
</script>

<style lang="scss" scoped>

</style>