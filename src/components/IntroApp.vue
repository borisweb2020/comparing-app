<template>
	<section class="intro">
		<div class="intro__content">
			<h2 class="intro__title">Смартфоны</h2>
			<nav class="intro__nav">
				<div class="intro__nav-title">Отобразить товары:</div>
				<ul class="intro__nav-amount">
					<li class="intro__nav-count"
					:class="{'active': count - 2 === index}"
					v-for="(i, index) in 5" :key="i + 1"
					@click="pointCount(index)">{{ i + 1 }}</li>
				</ul>
			</nav>
		</div>
		<div class="intro__content">
			<div class="intro__checkbox">
				<input class="intro__checkbox-input" type="checkbox" id="checkbox">
				<label class="intro__checkbox-label" for="checkbox">
					<span>Показать различия</span>
				</label>
			</div>
			<div class="intro__inner">

				<div class="intro__item" v-for="(item, index) in smarts" :key="index">
					<div class="intro__item-wrapper">
						<img class="intro__item-img" :src="item.url" alt="phone">
						<button class="intro__item-btn" type="button"
						@click="showModal(index)">
							<img src="../assets/images/arrow-down.svg" alt="arrow">
						</button>
					</div>
					<div class="intro__item-name">{{ item.producer }}</div>
					<modal-app v-if="modalWindow && modalIndex === index"
					:modalIndex="modalIndex"
					@closeModal="hideModal"></modal-app>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
	import ModalApp from '@/components/ModalApp.vue';

	export default {
		components: {
			ModalApp,
		},

		data(){
			return{
				count: 3,
				modalWindow: false,
				modalIndex: null,
			}
		},

		methods: {
			pointCount(index){
				this.count = (index + 2);
				this.$emit('point', this.count);
			},
			showModal(value){
				this.modalWindow = true;
				this.modalIndex = value;
			},
			hideModal(value){
				this.modalWindow = value;
			}
		},

		props: {
			smarts: {
				type: Array,
				required: true
			},

		}
	}
</script>

<style lang="scss" scoped>

</style>