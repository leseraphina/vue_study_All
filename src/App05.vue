<template>
	<div>
		<button v-on:click="plus">click:{{ state.count }}</button>
		<button v-on:click="plus">click:{{ state.main.count }}</button>
	</div>
</template>

<script>
// 반응형 데이터reactive()-> 반응 객체 데이터 생성
import { reactive } from 'vue';
export default {
	setup() {
		const state = reactive({
			count: 0,
			main: {
				count: 0,
			},
		});
		const plus = () => {
			state.count++;
			state.main.count++;
		};
		return { state, plus };
	},
};
</script>

<style scoped></style>
