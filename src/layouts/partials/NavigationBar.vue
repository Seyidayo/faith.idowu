<template>
  <nav>
    <h2>Faith Idowu</h2>
    <toggle-theme />
  </nav>
</template>

<script>
import ToggleTheme from "~/components/ToggleTheme";
import ToggleNav from "~/components/ToggleNav";
export default {
  components: {
    ToggleTheme,
    ToggleNav
  }
};
</script>

<style lang="scss" scoped>
nav {
  h2 {
    font-size: 32px;
  }
  --max-padding: 50px;
  @media (max-width: 350px) {
    --max-padding: 10px;
  }
  position: fixed;
  z-index: 1;
  backdrop-filter: blur(0.9px);
  width: 100%;
  height: 55px;
  display: flex;
  justify-content: space-between;
  padding-inline: var(--max-padding);
  padding-block: 10px;
  @supports not (padding-inline: 10px) {
    padding: 10px var(--max-padding);
  }
}
</style>
