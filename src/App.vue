<template>
  <div class="head">
    <b-nav class="button1">
      <b-nav-item active>
        <b-button
          @click="toggleCarousel('showBahia')"
          variant="outline-primary"
        >
          Bahia</b-button
        >
      </b-nav-item>

      <b-nav-item>
        <b-button @click="toggleCarousel('showSP')" variant="outline-success">
          Sao Paulo
        </b-button></b-nav-item
      >
      <b-nav-item>
        <b-button @click="toggleCarousel('showRJ')" variant="outline-info"
          >Rio De Janeiro</b-button
        >
      </b-nav-item>
    </b-nav>

    <div>
      <bahia :show="showBahia" />
      <saoPaulo :show="showSP" />
      <RioJAN :show="showRJ" />
    </div>
    <!-- </component:> -->
  </div>
</template>
<script>
import Bahia from "./Bahia.vue";
// import nav from "./nav.vue";
import SaoPaulo from "./SaoPaulo.vue";
import RioJAN from "./RioJaneiro.vue";

export default {
  components: { Bahia, SaoPaulo, RioJAN },
  data() {
    return {
      showSP: true,
      showBahia: false,
      showRJ: false,
    };
  },
  methods: {
    toggleCarousel(carouselName) {
      this.showSP = false;
      this.showBahia = false;
      this.showRJ = false;

      this[carouselName] = true;
    },
  },
};
</script>

<style>
.head {
  width: auto;
  height: auto;
}
.button1 {
  display: grid;
  grid-template-columns: 200px 200px 200px;
  justify-content: end;
  background-color: black;
}
</style>
