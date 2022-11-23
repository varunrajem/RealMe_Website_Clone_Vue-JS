<template>
  <v-card color="transparent" flat tile>
 
    <v-tabs color="black"
      v-model="tab"
      grow
    >
      <v-tab
        v-for="item in items"
        :key="item"
      >
        {{ item.name }}
      </v-tab>
    </v-tabs>

    <v-tabs-items v-model="tab" >
      <v-tab-item
        v-for="item in items"
        :key="item"
        class="bgC"
      >
      <v-row v-if="item.imgs">
        <v-col cols="12" md="3" v-for="product, i in item.imgs" :key="i">
 
        <v-card 
          color="white"
       flat tile
        >
          <v-img :src="product.src" height="200px" contain ></v-img>
          <h2 class="d-flex justify-center font-weight-medium body-1">{{product.title}}</h2>
        <h4 class="d-flex justify-center body-2">{{product.desc}}</h4>
        <div class="d-flex justify-center py-4">
        
       <span class="caption">From</span>
       <span class=" font-weight-medium red--text" >{{product.price}}</span></div>
        </v-card>
        </v-col>
             </v-row>
      </v-tab-item>
    </v-tabs-items>
  </v-card>
</template>
<script>
  export default {
    data () {
      return {
        tab: null,
        items: [
          {name: 'recommended',
           imgs:[
              {
                title:'realme C21 Y',
                src:'https://image01.realme.net/general/20210803/1627970794478.png',
                desc: 'Triple Camera . Real performance',
                price:'₹9,499'                
              },
              {
                title:'realme C25 ',
                src:'https://image01.realme.net/general/20210519/1621424163546.png',
                desc: 'Powerful Processor. 6000mah Batt..',
                price:'₹10,999'
              },
              {
                title:'realme C25Y ',
                src:'https://image01.realme.net/general/20210928/1632817235526.png',
                desc: '50MP AI Camera. All-day Performa..',
                price:'₹10,999'
              },
              {
                title:'realme narzo 50A',
                src:'https://image01.realme.net/general/20210916/1631776707007.png',
                desc: 'Mighty Performance Inside',
                price:'₹11,499'
              },
                {
                  title:'realme 8i',
                  src:'https://image01.realme.net/general/20210903/1630653680914.png',
                  desc: '120Hz. Infinitely Smooth',
                  price:'₹13,999'                
                },
              {
                title:'realme narzo 30A',
                src:'https://image01.realme.net/general/20210611/1623400675833.png',
                desc: 'Unleash Peak Performance',
                price:'₹13,499'
              },
                {
                  title:'realme 8',
                  src:'https://image01.realme.net/general/20210323/1616485282573.png',
                  desc: 'In Style. Capture Infinity',
                  price:'₹15,999'
                },
                {
                title:'realme 8',
                src:'https://image01.realme.net/general/20210506/1620287407432.png',
                desc: '5G. Speed to Infinity',
                price:'₹15,499'
              },
           ]
          }, 
          {name: 'New Launches',
           imgs:[
              {
                title:'realme 9 PRO+',
                src:'https://image01.realme.net/general/20220131/1643635116029.png',
                desc: 'CAPTURE THE LIGHT',
                price:'₹24,999'
              },
              {
                title:'realme 9 PRO',
                src:'https://image01.realme.net/general/20220129/1643438199175.png',
                desc: 'CAPTURE THE LIGHT',
                price:'₹17,999'
              },
              {
                title:'realme 9i',
                src:'https://image01.realme.net/general/20220126/1643190140852.png',
                desc: 'Next-Level Power',
                price:'₹13,999'
              },
              {
                title:'realme C252_Y',
                src:'https://image01.realme.net/general/20211116/1637046340070.png',
                desc: '%)MP AI Camera.All-day Performa..',
                price:'₹10,999'
              },
              {
                title:'realme narzo 50A',
                src:'https://image01.realme.net/general/20210916/1631776707007.png',
                desc: 'Mighty Performance Inside',
                price:'₹11,499'
              },
              {
                title:'realme narzo 50i',
                src:'https://image01.realme.net/general/20210916/1631776407331.png',
                desc: 'Mighty Performance Inside',
                price:'₹7,499'
              },
              {
                title:'realme C25Y',
                src:'https://image01.realme.net/general/20210913/1631506702085.png',
                desc: '50MP al Camwera.All-day Performa..',
                price:'₹10,999'
              },
              {
                title:'realme 8i',
                src:'https://image01.realme.net/general/20210903/1630653680914.png',
                desc: "India's First Helio G9 Processor",
                price:'₹13,999'
              },
                         ]
          }, 
          {name: 'Best Sellers',
           imgs:[
              {
                title:'Realme Note 9',
                src:'https://image01.realme.net/general/20210519/1621424163546.png',
                desc: 'Triple Camera bhifegfuwg',
                price:'250000'
              },
              {
                title:'Realme Note 9',
                src:'https://image01.realme.net/general/20210519/1621424163546.png',
                desc: 'Triple Camera bhifegfuwg',
                price:'250000'
              },
              {
                title:'Realme Note 9',
                src:'https://image01.realme.net/general/20210519/1621424163546.png',
                desc: 'Triple Camera bhifegfuwg',
                price:'250000'
              },
           ]
          }, 
        
        ],
      
      }
    },
  }
</script>
<style>
/* Helper classes */
.basil {
  background-color: #FFFBE6 !important;
}
.basil--text {
  color: #356859 !important;
}
</style>