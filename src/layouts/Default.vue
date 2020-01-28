<template>
  <main class="layout">
    <!-- <navigation-bar /> -->
    <slot />
  </main>
</template>

<script>
import NavigationBar from "./partials/NavigationBar";
import Footer from "./partials/Footer";
export default {
  components: {
    NavigationBar,
    Footer
  }
};
</script>