<template>
  <main>
    <Header />
    <Hero />
    <Offer />
    <HowDoIWork />
    <Reference />
    <Footer />
  </main>
</template>

<script>
import Header from "./components/header/HeaderDefault.vue";
import Hero from "./components/hero/HeroIndex.vue";
import Offer from "./components/offer/offerIndex.vue";
import HowDoIWork from "./components/howDoIWork/HowDoIWork.vue";
import Reference from "./components/reference/ReferenceIndex.vue";
import Footer from "./components/footer/FooterDefault.vue";
export default {
  name: "App",
  components: {
    Header,
    Hero,
    Offer,
    HowDoIWork,
    Reference,
    Footer,
  },
};
</script>

<style lang="scss" src="./index.scss"></style>
