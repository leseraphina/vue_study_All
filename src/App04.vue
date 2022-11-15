<template>
	<div>
		<p>{{ counter }}</p>
		<p>{{ message }}</p>
		<p>
			<button @click="increment">click : {{ counter }}</button>
		</p>
	</div>
</template>

<script>
// setup() 함수 사용하기
import { onMounted, ref } from 'vue';
export default {
	setup() {
		console.log('start');
		const counter = ref(0);
		const message = ref('hellow');
		const increment = () => {
			counter.value++;
		};

		onMounted(() => {
			console.log('mount');
		});
		console.log('counter');
		return { counter, message, increment };
	},
};
</script>

<style scoped></style>
