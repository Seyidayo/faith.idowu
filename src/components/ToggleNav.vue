<template>
	<div class="nav">
		<button class="nav-button" :class="{ hide: show }" @click="show = true">
			Show
		</button>
		<div class="nav-dashboard" v-if="show">
			<button class="nav-button" @click="show = false">
				hide
			</button>
			<ul>
				<li>Resume</li>
			</ul>
		</div>
	</div>
</template>

<script>
export default {
	data() {
		return {
			show: false
		};
	}
};
</script>

<style lang="scss" scoped>
.hide {
	visibility: hidden;
}
.nav-dashboard {
	position: absolute;
	// z-index: 2;
	right: 10px;
	width: 200px;
	height: 400px;
	background: red;
}
</style>
