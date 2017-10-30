<template>
	<v-app toolbar--fixed toolbar >
		
		<!-- TOOLBAR -->
		<v-toolbar id="toolbar1" fixed class="transparent elevation-0 " >
			<v-flex lg4 style="width:20px">
				<v-toolbar-items class="" style="height:64px">
					<v-layout justify-center align-center >
						<v-btn id="btn_included" href="#included" class="white--text arrow hidden-sm-and-down" style="height: -webkit-fill-available;" flat>WHAT INCLUDED</v-btn>
						<v-btn id="btn_useit" href="#useit" class="white--text arrow hidden-sm-and-down" style="height: -webkit-fill-available;" flat>HOW TO USE IT</v-btn>
						<v-btn id="btn_benefits" href="#benefits" class="white--text arrow hidden-sm-and-down" style="height: -webkit-fill-available;" flat>OTHER BENEFITS</v-btn>
						<!--  -->
						<v-btn id="btn_included" href="#included" class="white--text arrow hidden-md-and-up" style="height: 45px; width: 45px;" flat icon><v-icon>explore</v-icon></v-btn>
						<v-btn id="btn_useit" href="#useit" class="white--text arrow hidden-md-and-up" style="height: 45px; width: 45px;" flat icon><v-icon>swap_calls</v-icon></v-btn>
						<v-btn id="btn_benefits" href="#benefits" class="white--text arrow hidden-md-and-up" style="height: 45px; width: 45px;" flat icon><v-icon>card_giftcard</v-icon></v-btn>
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

    <!-- CONTAINER VIDEO -->
    <v-container fluid id="home" style="margin:0; padding:0; height:-webkit-fill-available; background-color:black;">
    	<v-layout row wrap style="background: url('/portadalcp.png') no-repeat center fixed; background-size: cover;">
    		<v-flex xs12 sm12 md12 lg12>   			
    			<v-layout column align-center justify-center style="height:-webkit-fill-available;"r>
    				<img id="logoimg" src="~/assets/limalogowhite.png" class="shadowfilter"  style="width:auto;height:342px;"></img>
    			</v-layout>
    		</v-flex>
    		<v-flex xs12 sm12 md12 lg12>
    			<v-layout justify-center align-center style="margin:-70px">
    				<v-btn dark href="#included"  class="transparent arrow elevation-0 " style="height: 1px; width: 1px;" >
    					<img id="seemore" src="~/assets/seemore.png">
    				</v-btn>
    			</v-layout>
    		</v-flex>
    	</v-layout>
    </v-container>
    <main>
    	<nuxt/>
    </main>
  </v-app>
</template>

<script>
import $ from 'jquery'

export default {
  data () {
    return {}
  },
  beforeMount: () => {
    $('#mylogo').hide()
  },
  mounted: () => {
    var imageHeight = parseInt($('#logoimg').css('height'))
    var stopHeight = 62.84
    $(window).scroll(function () {
      var windowScroll = $(window).scrollTop()
      var newHeight = imageHeight - 0.9 * windowScroll
      var windowWidth = $(window).width()
      var windowHeight = $(window).height()
      var toplogo = $('#logoimg').offset().top
      toplogo = toplogo - 1
      console.log(stopHeight)
      console.log(windowScroll)
      console.log(newHeight)
      console.log(windowWidth)
      console.log(windowHeight)
      console.log(toplogo)
      if (windowScroll > windowHeight - 50 && windowScroll < (2 * windowHeight) - 50) {
        $('#mylogo').show()
        $('#toolbar1').removeClass('transparent')
        $('#toolbar1').css('background-color', '#00CBDB')
        $('#seemore').fadeOut()
      } else if (newHeight >= stopHeight) {
        if (windowScroll >= 10) {
          $('#seemore').fadeOut()
          $('#logoimg').show()
          $('#logoimg').css('height', newHeight)
          $('#toolbar1').css('background-color', 'transparent')
          $('#mylogo').hide(40)
        } else {
          $('#seemore').fadeIn()
          $('#logoimg').show()
          $('#logoimg').css('height', newHeight)
          $('#toolbar1').css('background-color', 'transparent')
          $('#mylogo').hide()
        }
      } else if (windowScroll >= toplogo - 5) {
        $('#mylogo').show()
        $('#logoimg').hide()
        $('#seemore').fadeOut()
      } else {
        $('#logoimg').show()
        $('#logoimg').css('height', stopHeight)
        $('#toolbar1').addClass('transparent')
        $('#toolbar1').css('background-color', 'transparent')
        $('#bb').addClass('orange')
        $('#bb').addClass('white--text')
        $('#mylogo').hide()
      }
    })
  }
}
</script>

<style>

#seemore {
  -webkit-animation: zoom 1s ease-in-out infinite alternate;
  animation: zoom 1s ease-in-out infinite alternate;
  height: 95px;
}

@-webkit-keyframes zoom {
  from {
    -webkit-transform: scale(1, 1);
  }
  50% {
    -webkit-transform: scale(1.2, 1.2);
  }
  to {
    -webkit-transform: scale(1, 1);
  }
}

@keyframes zoom {
 from {
  transform: scale(1, 1);
}
to {
 transform: scale(1.2, 1.2);
}
}
</style>