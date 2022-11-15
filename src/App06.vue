<template>
	<div>
		<p>{{ i }}</p>
		<p>{{ message }}</p>
		<p>
			<button v-on:click="addMessage">click</button>
		</p>
		<p></p>
	</div>
</template>

<script>
import { ref } from 'vue';
export default {
	setup() {
		let i = ref(1);
		// let str = reactive(1);
		let message = ref('welcome');
		const addMessage = () => {
			++i.value;
			message.value += i.value;
		};
		// console.log('str:', typeof str);
		console.log('message:', typeof message.value);
		console.log('i:', typeof i.value);
		return { i, message, addMessage };
	},
};
</script>

<style scoped></style>
