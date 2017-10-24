<template>
  <v-toolbar id="toolbar1" fixed class="transparent elevation-0 " >
      <v-flex lg4 style="width:20px">
        <v-toolbar-items class="" style="height: -webkit-fill-available;">
          <v-layout justify-center align-center >
            <v-btn id="btn_included" href="#included" class="white--text arrow hidden-sm-and-down" style="height: -webkit-fill-available;" flat>WHAT INCLUDED</v-btn>
            <v-btn id="btn_useit" href="#useit" class="white--text arrow hidden-sm-and-down" style="height: -webkit-fill-available;" flat>HOW TO USE IT</v-btn>
            <v-btn id="btn_benefits" href="#benefits" class="white--text arrow hidden-sm-and-down" style="height: -webkit-fill-available;" flat>OTHER BENEFITS</v-btn>
            <!--  -->
            <v-btn id="btn_included" href="#included" class="white--text arrow hidden-md-and-up" style="height: 45px; width: 45px;" flat icon><v-icon>explore</v-icon></v-btn>
            <v-btn id="btn_useit" href="#useit" class="white--text arrow hidden-md-and-up" style="height: 45px; width: 45px;" flat icon><v-icon>swap_calls</v-icon></v-btn>
            <v-btn id="btn_benefits" href="#benefits" class="white--text arrow hidden-md-and-up" style="height: 45px; width: 45px;" flat icon><v-icon>card_giftcard</v-icon></v-btn>
            <!-- MENU -->
           <!--  <v-menu offset-y open-on-hover bottom left full-width  class="hidden-md-and-up" style="display: inline-flex; align-items: center; text-align: center;">
              <v-btn style="height: 38px; width: 38px;" icon slot="activator" dark>
                <v-icon large>more_vert</v-icon>
              </v-btn>
              <v-layout justify-center align-center >
                <v-list>
                  <v-list-tile-content>
                    <v-list-tile v-for="item in items" :key="item.title" @click="">
                      <v-list-tile-title>{{ item.title }}</v-list-tile-title>
                    </v-list-tile>
                  </v-list-tile-content>
                </v-list>
              </v-layout>
            </v-menu> -->
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
            <!-- <v-btn id ="bb" class="arcoirisbutton orange lighten-3 white--text elevation-0 shadowfilter" style="left:10%" round>BUY NOW</v-btn>
            -->
            <v-btn id ="bb" class="arcoirisbutton orange lighten-3 white--text elevation-0 shadowfilter" style="left:10%; height: 45px; width: 45px; padding:0; font-size:16px" round>
              <b>BUY NOW</b>
            </v-btn>
            

          </v-layout>
        </v-toolbar-items>
      </v-flex>
    </v-toolbar>
</template>

<script>
export default {
  name: 'toolbar'
}
</script>

<style>

</style>

