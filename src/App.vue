<template>
	<h1>Vue Router Demo</h1>
	<navigation></navigation>
	<router-view></router-view>
</template>

<script>
import Navigation from "./components/Navigation.vue";
export default {
	components: {
		Navigation,
	},
};
</script>


<style>
.router-link {
	text-decoration: none;
	display: inline-block;
	padding: 10px;
	box-sizing: border-box;
	border: 1px solid transparent;
	cursor: pointer;
}

.router-link:hover {
	border-bottom: 1px solid red;
	background-color: rgba(0, 0, 0, 0.1);
}

.cursor-pointer {
	cursor: pointer;
}
</style>