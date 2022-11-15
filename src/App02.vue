<template>
	<div>
		<button v-on:click="increment">카운트 : {{ counter }}</button>
	</div>
</template>

<script>
import { onMounted, ref } from 'vue';

export default {
	setup() {
		const counter = ref(0);
		// const increment = () => {
		// 	return counter.value ++;
		// };
		const increment = () => counter.value++;
		onMounted(() => {
			console.log('마운트가 끝났습니다.');
		});
		return { counter, increment };
	},
};
</script>

<style scoped></style>
