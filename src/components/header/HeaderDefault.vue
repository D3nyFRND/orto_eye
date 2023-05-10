<template>
  <nav class="navbar sticky-top bg-body-tertiary">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">
        <img
          src="../../assets/logo.svg"
          alt="ortoEYE leczenie zeza i niedowidzenia"
          class="logo"
        />
      </a>
      <ul class="menu" :class="{ sidebar: active === true }">
        <li>
          <a href="#" class="nav-link">O mnie</a>
        </li>
        <li>
          <a href="#" class="nav-link">Badania, Diagnoza, Terapia</a>
        </li>
        <li>
          <a href="#" class="nav-link">Cennik</a>
        </li>
        <li>
          <a href="#" class="nav-link">Warto wiedzieć</a>
        </li>
        <li>
          <a href="#" class="nav-link">Jak pracuję</a>
        </li>
        <li>
          <a href="#" class="nav-link">Galeria</a>
        </li>
        <li>
          <a href="#" class="nav-link">Kontakt</a>
        </li>
      </ul>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        fill="currentColor"
        class="hamburger"
        :class="{ sidebar: active === true }"
        viewBox="0 0 16 16"
        v-on:click="menu"
      >
        <path
          fill-rule="evenodd"
          d="M2.5 12a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5z"
        />
      </svg>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        fill="currentColor"
        class="hamburger phone"
        :class="{ sidebar: active === false }"
        viewBox="0 0 16 16"
        v-on:click="menu"
      >
        <path
          d="M2.146 2.854a.5.5 0 1 1 .708-.708L8 7.293l5.146-5.147a.5.5 0 0 1 .708.708L8.707 8l5.147 5.146a.5.5 0 0 1-.708.708L8 8.707l-5.146 5.147a.5.5 0 0 1-.708-.708L7.293 8 2.146 2.854Z"
        />
      </svg>
    </div>
  </nav>
  <section style="height: 200vh"></section>
</template>
<script>
export default {
  data() {
    return {
      active: false,
    };
  },
  methods: {
    menu() {
      this.active = !this.active;
    },
  },
};
</script>
<style lang="scss" src="./header.scss" scoped></style>
