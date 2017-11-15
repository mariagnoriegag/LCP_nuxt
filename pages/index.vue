<template>

  <div>
    <buycart></buycart>
    <v-container id="" fluid style="" class="withoutmargins">
      <v-layout row wrap justify-center align-center class="allwindow" style="padding-top:1%;padding-bottom:1%;  background-size: auto 100%;">
        <!-- TOOLBAR -->
        <v-toolbar id="toolbar1" fixed class="transparent elevation-0 " >
          <v-flex lg4 style="width:20px">
            <v-toolbar-items class="" style="height:64px">
              <v-layout justify-center align-center >
                <v-btn id="btn_included" href="#included" class="allwindow white--text arrow hidden-sm-and-down" style="" flat>WHAT INCLUDED</v-btn>
                <v-btn id="btn_useit" href="#useit" class="allwindow white--text arrow hidden-sm-and-down" style="" flat>HOW TO USE IT</v-btn>
                <v-btn id="btn_benefits" href="#benefits" class="allwindow white--text arrow hidden-sm-and-down" style="" flat>OTHER BENEFITS</v-btn>
                <!--  -->
                <v-btn id="btn_included" href="#included" class="btnsize_toolbar white--text arrow hidden-md-and-up" style="" flat icon><v-icon>explore</v-icon></v-btn>
                <v-btn id="btn_useit" href="#useit" class="btnsize_toolbar white--text arrow hidden-md-and-up" style="" flat icon><v-icon>swap_calls</v-icon></v-btn>
                <v-btn id="btn_benefits" href="#benefits" class="btnsize_toolbar white--text arrow hidden-md-and-up" style="" flat icon><v-icon>card_giftcard</v-icon></v-btn>
              </v-layout>
            </v-toolbar-items>
          </v-flex>
          <v-flex lg4 style="width:20px">
            <v-layout justify-center>
              <v-btn dark href="#home"  class="transparent arrow elevation-0 white--text " style="height: 50%; width: auto;" >
                <img id="mylogo" src="~/assets/limalogowhite.png" class=""  style="width:55px;"></img>
              </v-btn>
            </v-layout>
          </v-flex>
          <v-flex lg4 style="width:20px">
            <v-toolbar-items class="">
              <v-layout justify-center align-center>
                <v-btn href="#" class="white--text" style="height: 38px; width: 38px;" icon><v-icon>person</v-icon></v-btn>
                <v-btn id ="bb" class="arcoirisbutton orange lighten-3 white--text elevation-0 shadowfilter" style="left:10%; height: 45px; width: 45px; padding:0; font-size:16px" round>
                  <b>BUY NOW</b>
                </v-btn>
              </v-layout>
            </v-toolbar-items>
          </v-flex>
        </v-toolbar>
      </v-layout>
    </v-container>
    <!-- MAIN -->
    <main >
      
      <!-- INCLUDED -->
      <v-container id="included" fluid style="" class="withoutmargins">
          <v-layout row wrap justify-center align-center class="allwindow" style="padding-top:1%;padding-bottom:1%;  background-size: auto 100%;">
          </v-layout>
      </v-container>
      <!-- HOW TO USE IT -->
      <v-container id="useit" fluid style="" class="withoutmargins">
          <v-layout row wrap justify-center align-center class="allwindow" style="padding-top:1%;padding-bottom:1%;  background-size: auto 100%;">
          </v-layout>
      </v-container>
      <!-- OTHER BENEFITS -->
      <v-container id="benefits" fluid style="" class="withoutmargins">
          <v-layout row wrap justify-center align-center class="allwindow white" style="padding-top:1%;padding-bottom:1%;  background-size: auto 100%;">
          </v-layout>
      </v-container>
      <!-- FOOTER -->
      <v-container fluid  style="margin:0; padding:0;" fluid class="container-footer">
        <v-flex sm12 xl12 xs12 md12>
        </v-flex>
      </v-container>
    </main>

  </div>
</template>

<script> 
import $ from 'jquery'
import Buycart from '~/components/Buycart.vue'

export default {
  layout: 'landingbase',
  components: {
    Buycart
  },
  mounted: () => {
    $('.arrow').on('click', function () {
      $('html, body').animate({scrollTop: $($(this).attr('href')).offset().top}, 500, 'linear')
    })
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
.allwindow {
  height: -webkit-fill-available;
}
.btnsize_toolbar {
  height: 45px; 
  width: 45px;
}
.withoutmargins{
  margin:0; 
  padding:0;
}
.container-footer {
  display: table;
  width: 100%;
}
</style>
