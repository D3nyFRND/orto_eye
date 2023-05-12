<template>
  <main>
    <Header />
    <Hero />
    <Offer />
  </main>
</template>

<script>
import Header from "./components/header/HeaderDefault.vue";
import Hero from "./components/hero/HeroIndex.vue";
import Offer from "./components/offer/offerIndex.vue";
export default {
  name: "App",
  components: {
    Header,
    Hero,
    Offer,
  },
};
</script>

<style lang="scss" src="./index.scss"></style>
