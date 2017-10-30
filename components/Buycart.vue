<template>
  <v-flex id="cart" xs12 sm4 md4 lg4  style="position: fixed; top: 5em; right: 10px;">
    <div class="app active" style="margin:0; position: fixed; right: 10px;">
      <div>
        <div class="cust-info" style="margin-bottom:10px; margin-top:10px">
          <h2 style="font-size:14px; margin:0; padding:0">Get your tickets now and enjoy Lima!</h2>

        </div>
      </div>
      <div class="maindiv">
      </div>
      <v-layout row wrap justify-center align-center class="footerdiv round elevation-0" style="">
        <h2 class="white--text center" style="font-size:18px; font-weight:600">LIMA CITY PASS</h2>
        <ul style="height: 50px; width: auto;">
          <li class="white--text li_li" style="height:auto"> 
            <v-flex xs12 sm12 md12 xl12>
              <form id="myform" method="POST" action="">
                <v-btn icon flat class="transparent qtyminus" field="quantity">
                  <v-icon large class="orange--text text--accent-1">remove_circle</v-icon>
                </v-btn>
                <input type="text" value="0" class="qty" name="quantity"></input>
                <v-btn icon flat class="transparent qtyplus" field="quantity">
                  <v-icon large class="orange--text text--accent-1">add_circle</v-icon>
                </v-btn>
              </form>
            </v-flex>
          </li>
        </ul>
        <v-flex xs6 sm6 md6 xl6>
          <div class="white--text total" style="margin:0;border-top:0">
            <p>Total  <span id="total"> 0 </span> <span > $ </span></p>
          </div>
        </v-flex>
      </v-layout>
      <div class="maindiv2">
      </div>
      <div class="footerdiv2">
        <v-flex xs12 sm12 md12 lg12 style="margin:0; padding:0; border-top:0" class="buy_now">
          <v-layout justify-center align-center style="padding-bottom:0px; display: grid;">
            <v-btn id ="buynow" class="pink lighten-2 white--text elevation-0 shadowfilter" style="" round>PROCEED TO CHECKOUT</v-btn>
          </v-layout>
        </v-flex>
      </div>
    </div>
  </div>
</v-flex>
</template>
<script>
export default {
  name: 'buycart'
}
</script>
<style>
/* BUTTON BUY NOW CART */

.center {
  text-align: center;
}

.app {
  display: flex;
  flex-flow: column;
  margin: 50px auto 0;
  width: 300px;
  opacity: 0;
  transform: scale(0);
  transform-origin: top center;
  transition: all 0.8s cubic-bezier(.71, 0, .61, 1.36) 1.8s;
}

.app > * {
  /* don't use universal selectors at real world project. its known to be slow */
  background: #fff;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
}

.cust-info {
  margin: 15px 0;
  padding: 0 30px;
  position: relative;
  opacity: 0;
  transform: translateY(20px);
  transition: all 0.5s ease 2s;
  overflow: hidden;
}

.cust-info h3 {
  font-weight: 400;
}

.cust-info p {
  color: #757575;
  font-size: 12px;
  padding: 10px 0 0;
}

.cust-info:before {
  content: '';
  position: absolute;
  height: 100%;
  width: 6px;
  background: rgb(0, 157, 223);
  left: -20px;
  transition: all 0.5s ease 2s;
}


.li_li {
  color: #707575;
  font-size: 12px;
  list-style: none;
  height: auto;
  width: auto;
  opacity: 0;
  transform: translateX(-20px);
  transition: all 0.8s ease;
}

.li_li:nth-child(1) {
  transition-delay: 0.6s;
}

.li_li:not(:last-child) {
  border-bottom: 1px dashed #ccc;
  margin-bottom: 5px;
}

.li_li i {
  font-style: normal;
}

.total {
  border-top: 2px solid #FFC107;
  padding-top: 15px;
  margin: 0 0 15px;
  font-size: 14px;
  text-transform: uppercase;
  font-weight: 700;
  position: relative;
  left: -50px;
  opacity: 0;
  transform: translateY(10px);
  transition: left 0.5s ease, opacity 0.5s ease, transform 0s ease 1.8s;
}

.buy_now {
  border-top: 2px solid #FFC107;
  padding-top: 15px;
  margin: 0 0 15px;
  font-size: 14px;
  text-transform: uppercase;
  font-weight: 700;
  position: relative;
  left: -50px;
  opacity: 0;
  transform: translateY(10px);
  transition: left 0.1s ease, opacity 0.1s ease, transform 0s ease 1.8s;
}

.total p {
  opacity: 0;
  transform: translateY(10px);
  transition: all 0s ease 1.2s;
}
.total span {
  float: right;
}

.maindiv {
  border-bottom: 2px dotted #F06292;
  border-radius: 0 0 4px 4px;
  padding: 0 30px;
  position: relative;
  transform: perspective(1000px) rotateX(-90deg);
  transform-origin: top;
  transition: all 0.5s ease 1.7s;
}

.maindiv2 {
  border-bottom: 2px dotted #F06292;
  border-radius: 0 0 4px 4px;
  padding: 0 30px;
  position: relative;
  transform: perspective(1000px) rotateX(-90deg);
  transform-origin: top;
  transition: all 0.5s ease 1.1s;
}

.maindiv h3 {
  font-size: 18px;
  font-weight: 500;
  opacity: 0;
  margin: 15px 0;
  transform: translateY(10px);
  transition: all 0.5s ease 0.8s;
}

.maindiv:before {
  content: '';
  position: absolute;
  top: -2px;
  width: 100%;
  height: 2px;
  left: 0;
  background: #fff;
}

.footerdiv {
  border-radius: 4px;
  padding: 15px 30px;
  transform: perspective(1000px) rotateX(-90deg);
  transform-origin: top;
  transition: all 0.5s cubic-bezier(.42, -1.04, .79, 1) 1.1s;
}
.footerdiv2 {
  border-radius: 4px;
  padding: 15px 30px;
  transform: perspective(1000px) rotateX(-90deg);
  transform-origin: top;
  transition: all 0.5s cubic-bezier(.42, -1.04, .79, 1) 0.5s;
}

.footerdiv svg {
  fill: #757575;
}

.active {
  opacity: 1;
  transform: scale(1);
  transition: all 0.8s ease;
}

.active .cust-info {
  opacity: 1;
  transform: translateY(0);
  transition: all 1s ease 0.5s;
}

.active .cust-info:before {
  left: 0;
  transition: all 1s ease 0.7s;
}

.active .maindiv {
  transform: perspective(1000px) rotateX(0deg);
  transition: all 0.5s ease 0.5s;
}

.active .maindiv2 {
  transform: perspective(1000px) rotateX(0deg);
  transition: all 0.5s ease 0.9s;
}

.active .maindiv h3 {
  opacity: 1;
  transform: translateY(0);
  transition: all 0.8s ease 0.8s;
}

.active li {
  opacity: 1;
  transform: translateX(0px);
  transition: all 0.5s ease;
}

.active li:nth-child(1) {
  transition-delay: 1s;
}

.active .total {
  opacity: 1;
  transform: translateY(0);
  left: 0;
  transition: transform 0.5s ease 0.7s, opacity 0.5s ease 0.7s;
}

.active .buy_now {
  opacity: 1;
  transform: translateY(0);
  left: 0;
  transition: transform 1s ease 1.4s, opacity 1s ease 1.4s;
  transition-delay: 1.3s;
}

.active .total p {
  opacity: 1;
  transform: translateY(0);
  transition: all 0.3s ease 0.9s;
}
.active .footerdiv {
  transform: perspective(1000px) rotateX(0deg);
  transition: all 0.5s ease 0.5s;
}

.active .footerdiv2 {
  transform: perspective(1000px) rotateX(0deg);
  transition: all 0.5s ease 1.1s;
}
div.round {
  background: 
  linear-gradient(0deg, transparent 0px, #ED1862 0) left,
  linear-gradient(0deg, transparent 0px, #ED1862 0) right;  
  background-repeat: no-repeat;
  background-image:
  radial-gradient(circle at 0 50%, rgba(204,0,0,0) 14px, #F06292 15px),
  radial-gradient(circle at 100% 50%, rgba(204,0,0,0) 14px, #F06292 15px);
  background-size: 50% 100% 
}
.container-footer {
  display: table;
  width: 100%;
}
.column-footer {
  display: table-cell;
}
a:hover{
  color: cyan;
}
a:active{
  color: teal;
}
a {
  color: white;
}
a {
  text-decoration: none
}

</style>