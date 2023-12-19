<template>
	<section class="table">
		<div class="container">
			<div class="table__inner">
				<div class="table__header">
					<div class="table__header-item">Производитель</div>
					<div class="table__header-item">Год релиза</div>
					<div class="table__header-item">Диагональ экрана (дюйм)</div>
					<div class="table__header-item">страна-производитель</div>
					<div class="table__header-item">объем памяти</div>
					<div class="table__header-item">частота обновления экрана</div>
					<div class="table__header-item">nfc</div>
					<div class="table__header-item">поддержка esim</div>
					<div class="table__header-item">поддержка беспроводной зарядки</div>
					<div class="table__header-item">стоимость</div>
				</div>
				<div class="table__smart"
				v-for="(item, index) in smarts" :key="index">
					<div class="table__smart-item">{{ item.producer.split(' ')[0] }}</div>
					<div class="table__smart-item">{{ item.release }}</div>
					<div class="table__smart-item">{{ item.diagonal }}</div>
					<div class="table__smart-item">{{ item.state }}</div>
					<div class="table__smart-item">{{ item.memory }}</div>
					<div class="table__smart-item">{{ item.refresh }}</div>
					<div class="table__smart-item">
						<img v-if="item.nfc" src="../assets/images/check-green.svg" alt="true mark">
						<img v-else src="../assets/images/deny-red.svg" alt="false mark">
					</div>
					<div class="table__smart-item">
						<img v-if="item.esim" src="../assets/images/check-green.svg" alt="true mark">
						<img v-else src="../assets/images/deny-red.svg" alt="false mark">
					</div>
					<div class="table__smart-item">
						<img v-if="item.charging" src="../assets/images/check-green.svg" alt="true mark">
						<img v-else src="../assets/images/deny-red.svg" alt="false mark">
					</div>
					<div class="table__smart-item">{{ item.price }}</div>
				</div>
			</div>
		</div>
	</section>
</template>

<script>

	export default {
		props: {
			smarts: {
				type: Array,
				required: true
			}
		}
	}
</script>

<style lang="scss" scoped>

</style>