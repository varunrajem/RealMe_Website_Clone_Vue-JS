<template>
  <v-container>
    <AllProductsCard :allProducts="models" />
  </v-container>
</template>

<script>
import AllProductsCard from "@/components/Products/Product.vue";
export default {
  components: {
    AllProductsCard,
  },
  data() {
    return {
      models: [
         {
           src: "https://image01.realme.net/general/20211011/1633945837036.png",
           title:"realme Micro-USB Cable",
           desc:"₹199",
           slug:"cable"
         },
         {
           src: "https://image01.realme.net/general/20211011/1633945684839.png",
            title:"realme Type-C Cable",
           desc:"₹249",
           slug: "cable1"
         },
         {
           src: "https://image01.realme.net/general/20211022/1634885772461.png",
            title:"realme Buds Air Neo",
           desc:"₹399"
         },
         {
           src: "https://image01.realme.net/general/20210223/1614057007991.png",
            title:"realme Moblie Game C.",
           desc:"₹999"
         },
         {
           src: "https://image01.realme.net/general/20201223/1608696018552.jpg",
            title:"realme T-shirt",
           desc:"₹999"
         },
         {
           src: "https://image01.realme.net/general/20210223/1614059229445.png",
            title:"realmeow Cap",
           desc:"₹999"
         },
         {
           src: "https://image01.realme.net/general/20210223/1614063237784.jpg",
            title:"realmeow T-shirt",
           desc:"₹999"
         },
         {
           src: "https://image01.realme.net/general/20200612/1591953520295.jpg",
            title:"realme Backpack",
           desc:"₹1,499"
         },
         {
           src: "https://image01.realme.net/general/20200817/1597675424246.jpg",
            title:"realme T-shirt",
           desc:"₹999"
         },
         {
           src: "https://image01.realme.net/general/20190105/1546660465921.jpg",
            title:"realme Backpack",
           desc:"₹2,399"
         },
         {
           src: "https://image01.realme.net/general/20200825/1598343953637.jpg",
            title:"realme Tote Bag 2",
           desc:"₹999"
         },        
       ],
    }
  }
};
</script>

<style>

</style>