<template>
	<section>
		<Ruler />
		<header class="center">
			<p class="description">
				I'm a {{ new Date().getFullYear() - 1999 }} year old developer from
				Lagos Nigeria with over {{ new Date().getFullYear() - 2019 }}+ years of
				experience building applications using core
				<b>front-end technologies</b>
				(HTML, CSS and JS).
			</p>
		</header>
		<Ruler />
	</section>
</template>

<script>
import Ruler from "~/components/Ruler";
export default {
	components: {
		Ruler
	}
};
</script>

<style lang="scss" scoped></style>
