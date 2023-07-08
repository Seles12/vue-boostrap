<template>
  <div class="nav">
    <b-nav>
      <b-nav-item active>
        <b-button @click="toggleCarousel('showBahia')" variant="outline-primary">Sao Paulo</b-button>
      </b-nav-item>
      
      <b-nav-item>
        <b-button @click="toggleCarousel('showSP')" variant="outline-success"
          >Rio De Janeiro</b-button
        ></b-nav-item
      >
      <b-nav-item>
        <b-button @click="toggleCarousel('showRJ')" variant="outline-info">Bahia</b-button>
      </b-nav-item>
    </b-nav>

    <div>
      <bahia :show="showBahia"/>
      <saoPaulo :show="showSP"/>
      <RioJAN :show="showRJ"/>
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
    }
  },
  methods: {
    toggleCarousel(carouselName) {
      this.showSP = false;
      this.showBahia = false;
      this.showRJ = false;

      this[carouselName] = true;
    }
  }
};
</script>

<style>
.nav {
  display: flex;
    justify-content: flex-end;
    background: black;
    flex-direction: column;
}
</style>
