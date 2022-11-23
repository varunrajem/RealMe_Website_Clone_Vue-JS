<template>
  <div class="bgC">
    <v-divider class="my-1"></v-divider>

    <v-container>
      <v-btn text
        ><v-img src="@/assets/realme.png" width="70px"></v-img>
      </v-btn>

      <span v-for="(link, i) in navLinks" :key="i" class="px-5">
        <span class="body-2">{{ link }}</span>
      </span>
      <v-icon>mdi-magnify</v-icon>
    </v-container>

    <v-row>
      <v-col cols="12">
        <v-carousel
          cycle
          class="mb=10"
          :show-arrows-on-hover="true"
          height="700"
          hide-delimiters
        >
          <v-carousel-item
            v-for="(item, i) in items"
            :key="i"
            :src="item.src"
          ></v-carousel-item>
        </v-carousel>
      </v-col>
    </v-row>

    <h3 class="ml-16 mt-12">ONLY HERE</h3>
    <v-sheet class="mx-auto" color="transparent">
      <v-slide-group
        v-model="model"
        class="pa-4"
        active-class="success"
        show-arrows
      >
        <v-slide-item v-for="(model, i) in models" :key="i">
          <v-card
            @click="$router.push(`/${model.slug}`)"
            class="ma-4"
            height="400"
            width="300"
          >
            <v-img :src="model.src" contain></v-img>
            <h2 class="d-flex justify-center font-weight-light">
              {{ model.title }}
            </h2>
            <h2 class="d-flex justify-center font-weight-bold red--text">
              {{ model.desc }}
            </h2>
          </v-card>
        </v-slide-item>
      </v-slide-group>
    </v-sheet>
    <v-container>
      <h2>Smartphones</h2>

      <Tabs />

      <h2 class="mx-12 font-weight-medium body-4">Smart Life</h2>

      <Card />
    </v-container>
  </div>
</template>

<script>
import Tabs from "@/components/Tabs.vue";
import Card from "@/components/card.vue";
export default {
  components: {
    Tabs,
    Card,
  },
  data() {
    return {
      models: [
        {
          src: "https://image01.realme.net/general/20211011/1633945837036.png",
          title: "realme Micro-USB Cable",
          desc: "₹199",
          slug: "cable",
        },
        {
          src: "https://image01.realme.net/general/20211011/1633945684839.png",
          title: "realme Type-C Cable",
          desc: "₹249",
          slug: "cable1",
        },
        {
          src: "https://image01.realme.net/general/20211022/1634885772461.png",
          title: "realme Buds Air Neo",
          desc: "₹399",
        },
        {
          src: "https://image01.realme.net/general/20210223/1614057007991.png",
          title: "realme Moblie Game C.",
          desc: "₹999",
        },
        {
          src: "https://image01.realme.net/general/20201223/1608696018552.jpg",
          title: "realme T-shirt",
          desc: "₹999",
        },
        {
          src: "https://image01.realme.net/general/20210223/1614059229445.png",
          title: "realmeow Cap",
          desc: "₹999",
        },
        {
          src: "https://image01.realme.net/general/20210223/1614063237784.jpg",
          title: "realmeow T-shirt",
          desc: "₹999",
        },
        {
          src: "https://image01.realme.net/general/20200612/1591953520295.jpg",
          title: "realme Backpack",
          desc: "₹1,499",
        },
        {
          src: "https://image01.realme.net/general/20200817/1597675424246.jpg",
          title: "realme T-shirt",
          desc: "₹999",
        },
        {
          src: "https://image01.realme.net/general/20190105/1546660465921.jpg",
          title: "realme Backpack",
          desc: "₹2,399",
        },
        {
          src: "https://image01.realme.net/general/20200825/1598343953637.jpg",
          title: "realme Tote Bag 2",
          desc: "₹999",
        },
      ],
      navLinks: [
        "realme Smartphones",
        "narzo Smartphones",
        "realme TV",
        "Laptop & Tablet",
        "Audio",
        "Smart Life",
        "Accessories & Lifestyle",
      ],
      items: [
        {
          src: require("@/assets/a.jpg"),
        },
        {
          src: require("@/assets/s.jpg"),
        },
        {
          src: require("@/assets/d.jpg"),
        },
        {
          src: "https://image01.realme.net/general/20220216/1644998133736.jpg",
        },
        {
          src: "https://image01.realme.net/general/20220216/1644998170734.jpg",
        },
        {
          src: "https://image01.realme.net/general/20220221/1645421088220.jpg",
        },
      ],
      links: [
        {
          img: "https://image01.realme.net/general/20210803/1627970794478.png",
        },
        {
          img: "https://image01.realme.net/general/20210519/1621424163546.png",
        },
      ],
    };
  },
};
</script>

<style >
.bgC {
  background-color: aliceblue;
}
</style>