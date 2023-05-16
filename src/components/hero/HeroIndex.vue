<template>
  <section>
    <div
      v-if="modalToogle_value_knowMore"
      class="knowMore"
      :class="{ modal: modalToogle_value_knowMore == true }"
      v-on:click.self="modalToogle_knowMore"
    >
      <div class="knowMore_inside">
        <h1>Lorem, ipsum.</h1>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Animi,
          aperiam.
        </p>
      </div>
    </div>
    <div
      v-if="modalToogle_value_playButton"
      class="playButton"
      :class="{ modal: modalToogle_value_playButton == true }"
      v-on:click.self="modalToogle_playButton"
    >
      <div class="playButton_inside">
        <iframe
          width="560"
          height="315"
          src="https://www.youtube.com/embed/dQw4w9WgXcQ"
          title="YouTube video player"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
          allowfullscreen
        >
        </iframe>
      </div>
    </div>
    <div class="left">
      <div>
        <div class="leftText">
          <h2>Specjalistyczny</h2>
          <h1>Gabinet Ortoptyczny w Olsztynie</h1>
        </div>
        <button v-on:click="modalToogle_knowMore">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="bi-caret-right-fill"
            viewBox="0 0 16 16"
          >
            <path
              d="m12.14 8.753-5.482 4.796c-.646.566-1.658.106-1.658-.753V3.204a1 1 0 0 1 1.659-.753l5.48 4.796a1 1 0 0 1 0 1.506z"
            />
          </svg>
          <span>dowiedz się więcej</span>
        </button>
      </div>
    </div>
    <div class="right">
      <div class="empty"></div>
      <div class="boxes">
        <div class="boxesTop">
          <div class="boxLeft box"></div>
          <div class="boxRight box">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="bi bi-eye"
              viewBox="0 0 16 16"
            >
              <path
                d="M16 8s-3-5.5-8-5.5S0 8 0 8s3 5.5 8 5.5S16 8 16 8zM1.173 8a13.133 13.133 0 0 1 1.66-2.043C4.12 4.668 5.88 3.5 8 3.5c2.12 0 3.879 1.168 5.168 2.457A13.133 13.133 0 0 1 14.828 8c-.058.087-.122.183-.195.288-.335.48-.83 1.12-1.465 1.755C11.879 11.332 10.119 12.5 8 12.5c-2.12 0-3.879-1.168-5.168-2.457A13.134 13.134 0 0 1 1.172 8z"
              />
              <path
                d="M8 5.5a2.5 2.5 0 1 0 0 5 2.5 2.5 0 0 0 0-5zM4.5 8a3.5 3.5 0 1 1 7 0 3.5 3.5 0 0 1-7 0z"
              />
            </svg>
            <p class="paragraph">Profesjonalne badania i terapia wzroku</p>
          </div>
        </div>
        <div class="boxesBottom">
          <div class="boxLeft box">
            <div>
              <span v-on:click="modalToogle_playButton">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="bi bi-play-fill"
                  viewBox="0 0 16 16"
                >
                  <path
                    d="m11.596 8.697-6.363 3.692c-.54.313-1.233-.066-1.233-.697V4.308c0-.63.692-1.01 1.233-.696l6.363 3.692a.802.802 0 0 1 0 1.393z"
                  />
                </svg>
              </span>
            </div>
          </div>
          <div class="boxRight box">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="bi bi-clock"
              viewBox="0 0 16 16"
            >
              <path
                d="M8 3.5a.5.5 0 0 0-1 0V9a.5.5 0 0 0 .252.434l3.5 2a.5.5 0 0 0 .496-.868L8 8.71V3.5z"
              />
              <path
                d="M8 16A8 8 0 1 0 8 0a8 8 0 0 0 0 16zm7-8A7 7 0 1 1 1 8a7 7 0 0 1 14 0z"
              />
            </svg>
            <p class="paragraph">Spokój i brak pośpiechu podczas badania</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  data() {
    return {
      modalToogle_value_knowMore: false,
      modalToogle_value_playButton: false,
    };
  },
  methods: {
    modalToogle_knowMore() {
      this.modalToogle_value_knowMore = !this.modalToogle_value_knowMore;
      if (this.modalToogle_value_knowMore == true) {
        document.querySelector("body").style.overflow = "hidden";
      } else {
        document.querySelector("body").style.overflow = "scroll";
      }
    },
    modalToogle_playButton() {
      this.modalToogle_value_playButton = !this.modalToogle_value_playButton;
      if (this.modalToogle_value_playButton == true) {
        document.querySelector("body").style.overflow = "hidden";
      } else {
        document.querySelector("body").style.overflow = "scroll";
      }
    },
  },
};
</script>

<style lang="scss" src="./hero.scss" scoped></style>
