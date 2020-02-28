<template>
  <Layout>
    <LazyHydrate when-idle>
      <home-hey />
    </LazyHydrate>
    <LazyHydrate when-visible>
      <home-what />
    </LazyHydrate>
    <LazyHydrate>
      <home-me />
    </LazyHydrate>
    <LazyHydrate>
      <Footer />
    </LazyHydrate>
  </Layout>
</template>

<script>
import LazyHydrate from "vue-lazy-hydration";
import HomeHey from "~/components/home/HomeHey";
import Footer from "~/layouts/partials/Footer";
export default {
  metaInfo: {
    title: "Portfolio"
  },
  components: {
    HomeHey,
    HomeWhat: () => import("~/components/home/HomeWhat"),
    HomeMe: () => import("~/components/home/HomeMe"),
    Footer,
    LazyHydrate
  }
};
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
