<template>
  <section class="container">
    <section>
      <article>
        <h2>Me?</h2>
        <p
          class="description"
        >Mostly I work using VueJs and React framework, however I am no stranger to a NodeJs server code, I love to pay attention to detail and try my best to iterate on Ideas in the shortest possible time</p>
        <p class="description">
          I’m simple! I like good articles, interesting food, drinking,
          <a
            href="https://duduke.substack.com"
          >good music</a>, engaging
          podcasts, learning about money, scrolling through TikTok, 90s sitcom
          and spending quality time with friends.
        </p>
        <p class="description">
          You can find me
          <a href="https://twitter.com/faithidowu_">retweeting</a> a lot of
          Nigerian tech gists, please
          <a
            href="mailto:faithid10@gmail.com"
          >contact me</a> if you would like
          to share awesome stuffs that are bursting your head right now - or you
          know, want to work with me.
        </p>
      </article>
      <figure>
        <img src="../../assets/images/circuit-board.svg" height="100%" width="100%" alt />
      </figure>
    </section>
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

<style lang="scss" scoped>
.container {
  padding-top: 4rem;

  section {
    display: grid;

    @media (min-width: 1024px) {
      grid-template-columns: 1fr 400px;
    }
    grid-gap: 35px;
    .description {
      inline-size: 100%;
      text-align: justify;
    }

    article {
      // padding-inline-end: ;
    }
  }

  figure {
    padding-inline-start: 1rem;
    img {
      opacity: 0.75;
    }
  }
}
</style>