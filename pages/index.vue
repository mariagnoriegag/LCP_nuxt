<template>
  <div>
    <buycart></buycart>
    <v-container style="height: -webkit-fill-available">
  </v-container>
  </div>
</template>

<script> 
// import $ from 'jquery'
import Buycart from '~/components/Buycart.vue'

export default {
  layout: 'landingbase',
  components: {
    Buycart
  }
}
/*  $(window).scroll(function() {
  var windowScroll = $(window).scrollTop(),
  newHeight = imageHeight - 0.9*windowScroll;

  var windowWidth = $( window ).width(),
  windowHeight = $( window ).height(),
  toplogo = $("#logoimg").offset().top;

  toplogo = toplogo-1;
} */
</script>

<style>

</style>
