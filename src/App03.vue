<template>
	<div>
		<h2>반응형 데이터</h2>
		<p>{{ reData }}</p>
		<p>
			<button v-on:click="reAction">click action</button>
		</p>
		<h2>일반데이터</h2>
		<p>{{ data }}</p>
		<!--  click시 error이 된다.  -->
		<p>
			<button v-on:click="dataAction">click action</button>
		</p>
	</div>
</template>

<script>
import { isRef, onBeforeMount, onMounted, ref } from 'vue';

export default {
	setup() {
		console.log('start');
		// 반응형 데이터
		const reData = ref(0);
		const reAction = () => {
			reData.value++;
		};
		// 일반데이터
		const data = 0;
		//
		let dataAction = () => {
			data = data++;
		};
		onMounted(() => {
			console.log('mount');
		});
		onBeforeMount(() => {
			console.log('beforeMount');
		});
		console.log(isRef(reData));
		console.log(isRef(data));
		return { reData, data, reAction, dataAction };
	},
};
</script>

<style scoped></style>
