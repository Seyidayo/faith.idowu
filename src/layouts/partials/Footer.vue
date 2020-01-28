<template>
  <footer class="container">
    <ul>
      <li>
        <a href="https://github.com/seyidayo">Github</a>
      </li>
      <li>
        <a
          href="https://docs.google.com/document/d/14aiG74XhxphzfW3ytktAowyGHGGeg4iQRl0V34OjfWA/edit?usp=sharing"
        >Resume</a>
      </li>
      <li>
        <a href="https://codepen.io/seyidayo/">CodePen</a>
      </li>
      <li>
        <a href="https://www.linkedin.com/in/faithidowu/">LinkedIn</a>
      </li>
      <li>
        <a href="https://twitter.com/faithidowu_">Twitter</a>
      </li>
    </ul>
    <p>
      &copy;
      {{ new Date().getFullYear() }}, Faith Idowu, Don't postpone fun.
    </p>
  </footer>
</template>
<style lang="scss" scoped>
p {
  margin-block-end: var(--min-padding);
}

footer {
  font-size: 1.2rem;
  ul {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
  }
  @media (min-width: 1024px) {
    text-align: center;
    ul {
      grid-template-columns: repeat(5, 1fr);
    }
  }
  padding-block-start: 4rem;
}
</style>
