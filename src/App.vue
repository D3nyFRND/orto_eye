<template>
  <main>
    <Header />
    <Hero />
  </main>
</template>

<script>
import Header from "./components/header/HeaderDefault.vue";
import Hero from "./components/hero/HeroIndex.vue";
export default {
  name: "App",
  components: {
    Header,
    Hero,
  },
};
</script>

<style lang="scss" src="./index.scss"></style>
