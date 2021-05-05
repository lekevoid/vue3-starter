<template>
	<div>
		<h1><em>Home</em> sweet <em>home</em></h1>
		<p>Name in store is : {{ name }}</p>
	</div>
</template>

<script setup>
import { computed } from "vue";
import { useStore } from "vuex";

const store = useStore();

const name = computed(() => {
	return store.state.user.name;
});
</script>

<style lang="scss">
h1 {
	color: #000;
	em {
		color: #f00;
		font-style: normal;
	}
}
</style>