<template>
  <v-row>
    <v-col cols="12"  v-for="(product, i) in allProducts" :key="i">
      <v-card width="10000">
        <v-img :src="product.src" height="200px" contain></v-img>
        <v-card-title>{{ product.title }}</v-card-title>
  <v-card-subtitle>{{product.desc}}</v-card-subtitle>

        <v-btn
          @click="$emit('addToCart', product)"
          class="ma-2"
          depressed
          color="warning"
          >Add To Cart</v-btn>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  props: { allProducts: Array },
};
</script>

<style></style>
