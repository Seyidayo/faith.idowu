<template>
  <Layout>
    <home-hey />
    <home-about />
    <home-what />
    <home-me />
    <Footer />
  </Layout>
</template>

<script>
import HomeHey from "~/components/home/HomeHey";
import HomeAbout from "~/components/home/HomeAbout";
import HomeWhat from "~/components/home/HomeWhat";
import HomeMe from "~/components/home/HomeMe";
import Footer from "~/layouts/partials/Footer";
export default {
  metaInfo: {
    title: "Welcome"
  },
  components: {
    HomeHey,
    HomeAbout,
    HomeWhat,
    HomeMe,
    Footer
  }
};
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
