<template>
  <header class="container">
    <section>
      <h1>
        Hi, my
        <br />name is Faith
      </h1>
      <p class="description">
        <b>Frontend Engineer</b>, Natterbase
      </p>
    </section>
    <div class="pattern-bg animation-reveal"></div>
  </header>
</template>
<style lang="scss" scoped>
@import "https://cdn.jsdelivr.net/npm/animate.css@3.5.1";
header {
  block-size: 100%;
  display: grid;
  @media (min-width: 1024px) {
    grid-template-columns: 1fr 1fr;
  }
}
section {
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 100%;
}
</style>
