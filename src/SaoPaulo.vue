<template>
  <div class="SaoPaulo" v-if="show">
    <b-carousel
      id="carousel-fade"
      style="text-shadow: 0px 0px 2px #000"
      indicators
      img-width="800"
      img-height="200"
    >
      <b-carousel-slide
        caption="BRASIL SAO PAULO"
        img-src="https://picsum.photos/id/88/1024/480"
      ></b-carousel-slide>
      <b-carousel-slide
        caption="BRASIL SAO PAULO MORIMBU"
        img-src="https://picsum.photos/id/183/1024/480"
      ></b-carousel-slide>
      <b-carousel-slide
        caption="BRASIL SAO PAULO CENTRO"
        img-src="https://picsum.photos/id/192/1024/480"
      ></b-carousel-slide>
    </b-carousel>
  </div>
</template>

<script>
export default {
  props: {
    show: Boolean,
  },
}
</script>

<style>
/* .SaoPaulo {
  display: none;
} */
</style>
