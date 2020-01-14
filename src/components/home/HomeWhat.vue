<template>
	<section>
		<h2>Latest works</h2>
		<div class="grid">
			<div class="grid-item" v-for="work in works" :key="work.no">
				<big>{{ work.no }}</big>
				<article>
					<p>
						<b>{{ work.title }} </b>
					</p>
					<p>
						{{ work.description }}
					</p>
					<a :href="work.link.live" v-if="work.link.live">website</a>
					<a :href="work.link.repository" v-if="work.link.repository"
						>repository</a
					>
				</article>
			</div>
		</div>
		<p class="description">
			Some of this sites are
			<a href="https://github.com/seyidayo">public on github</a>, if you'd like
			to follow along
		</p>
	</section>
</template>

<script>
export default {
	data() {
		return {
			works: [
				{
					no: "01",
					title: "Daily Sketches",
					description:
						"I take time out of my schedule to convert at least one dribbble or figma design using CSS",
					link: {
						live: "https://seyidayo.github.io/Daily-Sketches/",
						repository: "https://github.com/Seyidayo/Figma-Sketches"
					}
				},

				{
					no: "02",
					title: "Sportage shoes",
					description:
						"A minimal shoe store done to take a stab at this MERN stack every one is buzzing about",

					link: {
						live: "https://sportage.herokuapp.com",
						repository:
							"https://bitbucket.org/FaithIdowu/sportage-fe/src/master/"
					}
				},
				{
					no: "03",
					title: "Zoropay",
					description:
						"Zoropay helps students pay their school fees by offering a fair loan and payback system",
					link: { live: "https://zoropay.ng" }
				},
				{
					no: "04",
					title: "Breaking Bad",
					description:
						"Zoropay helps students pay their school fees by offering a fair loan and payback system",
					link: []
				}
			]
		};
	}
};
</script>

<style lang="scss" scoped></style>
