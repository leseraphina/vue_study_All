<template>
	<div>
		<button v-on:click="increment">카운트 : {{ counter }}</button>
	</div>
</template>

<script>
//  options composition
export default {
	data() {
		return {
			counter: 0,
		};
	},
	methods: {
		increment() {
			this.counter++;
		},
	},
	mounted() {
		console.log('마운트가 끝났습니다.');
	},
};
</script>

<style scoped></style>
