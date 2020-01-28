<template>
  <button type="button" @click="toggleTheme" :title="'Toggle ' + nextTheme">
    <svg
      v-if="theme === 'dark'"
      xmlns="http://www.w3.org/2000/svg"
      width="20"
      height="20"
      viewBox="0 0 24 24"
      fill="none"
      stroke="white"
      stroke-width="2"
      stroke-linecap="round"
      stroke-linejoin="round"
    >
      <path d="M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z" />
    </svg>
    <img v-else-if="theme === 'light'" width="24px" height="24px" alt :src="Sketch" />
  </button>
</template>

<script>
let themes = ["light", "dark"];
// import Sketch from "~/assets/images/pen.svg";
export default {
  data() {
    return {
      Sketch,
      theme: "light"
    };
  },
  computed: {
    nextTheme() {
      const currentIndex = themes.indexOf(this.theme);
      const nextIndex = (currentIndex + 1) % themes.length;
      return themes[nextIndex];
    }
  },
  methods: {
    toggleTheme() {
      const currentIndex = themes.indexOf(this.theme);
      const nextIndex = (currentIndex + 1) % themes.length;
      window.__setPreferredTheme(themes[nextIndex]);
      this.theme = themes[nextIndex];
    }
  },
  async mounted() {
    // set default
    if (typeof window.__theme !== "undefined") this.theme = window.__theme;
  }
};
</script>

<style lang="scss" scoped>
button {
  background: transparent;
  border: none;
  outline: none;
}
</style>
