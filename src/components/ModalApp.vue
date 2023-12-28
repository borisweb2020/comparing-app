<template>
	<div class="modal" @click="updateModal">
		<input  class="modal__input" type="text" placeholder="Поиск" @click.stop>
		<ul class="modal__list">
			<li class="modal__item">
				<button class="modal__btn" @click.stop>
					<img class="modal__btn-img" src="../assets/images/reverse-arrows.svg" alt="btn">
				</button>
				<div class="modal__item-wrapper">
					<img class="modal__item-img" src="../assets/images/samsung-72.jpg" alt="phone">
					<span class="modal__item-title">Samsung S21</span>
				</div>
			</li>
			<li class="modal__item">
				<button class="modal__btn">
					<img class="modal__btn-img" src="../assets/images/reverse-arrows.svg" alt="btn">
				</button>
				<div class="modal__item-wrapper">
					<img class="modal__item-img" src="../assets/images/samsung-72.jpg" alt="phone">
					<span class="modal__item-title">Xiaomi Mi 11 Lite</span>
				</div>
			</li>
			<li class="modal__item">
				<button class="modal__btn">
					<img class="modal__btn-img" src="../assets/images/reverse-arrows.svg" alt="btn">
				</button>
				<div class="modal__item-wrapper">
					<img class="modal__item-img" src="../assets/images/samsung-72.jpg" alt="phone">
					<span class="modal__item-title">Apple iPnone 11 Pro</span>
				</div>
			</li>
		</ul>
	</div>
</template>
<script>
	export default {
		methods: {
			updateModal(){
				const newValue = false;
				this.$emit('closeModal', newValue);
			}
		}
	}
</script>
<style lang="scss">

</style>