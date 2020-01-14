<template>
  <div>
    <navigation-bar />
    <main class="layout">
      <slot />
    </main>
  </div>
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