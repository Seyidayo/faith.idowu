<template>
  <header class="container">
    <section>
      <h1 class="animation-reveal-bottom">
        Hi, my
        <br />name is Faith
      </h1>
      <p class="description animation-fade">
        <b>Frontend Engineer</b>, Natterbase
      </p>
    </section>
    <!-- <div class="pattern-bg animation-reveal"></div> -->

    <header>
      <p class="description animation-fade" style="margin-top: 1.5rem">
        I'm a {{ new Date().getFullYear() - 1999 }} year old developer from
        Lagos Nigeria with over {{ new Date().getFullYear() - 2019 }}+ years of
        experience building applications using core
        <b>front-end technologies</b>
        (HTML, CSS and JS).
      </p>
      <p style="display: flex; flex-direction: row;">
        <a href="https://app.pluralsight.com/profile/FaithIdowu">Expert in HTML5 and CSS3</a>
        <img src="../../assets/images/pluralsight.png" height="auto" width="160px" alt />
      </p>
    </header>
  </header>
</template>
<style lang="scss" scoped>
@import "https://cdn.jsdelivr.net/npm/animate.css@3.5.1";
.container {
  padding-top: 7rem;
  block-size: 700px;
}
.description {
  margin: 1rem 0;
  @media (min-width: 700px) {
    inline-size: 80%;
  }
}
</style>
