<template>
  <div class="nav">
    <b-nav>
      <b-nav-item active>
        <b-button variant="outline-primary">Sao Paulo</b-button>
      </b-nav-item>
      <b-nav-item>
        <b-button variant="outline-success"
          >Rio De Janeiro</b-button
        ></b-nav-item
      >
      <b-nav-item>
        <b-button variant="outline-info">Bahia</b-button>
      </b-nav-item>
    </b-nav>
    -->
    <!-- <nav></nav>

    <!-- <button @click="show = !show">sao paulo</button> -->
    <bahia> </bahia>
    <saoPaulo></saoPaulo>
    <RioJAN></RioJAN>
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
  // props: ["Bahia", "SaoPaulo", "RioJAN"],
  // data() {
  //   return {
  //     show:false
  //   }

  // }
};
</script>

<style>
.nav {
  display: flex;
  justify-content: flex-end;
  background: black;
}
</style>
