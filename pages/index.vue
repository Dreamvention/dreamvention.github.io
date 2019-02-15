<template>
  <v-layout justify-center row>
    <v-flex  xs12 sm12 md10>
      <div>
        <Hero></Hero>
      </div>
      <v-layout justify-space-between row wrap>
        <v-flex xs12 sm12 md8 lg3 v-for="icon_thumb in icon_thumbs">
          <IconThumb :icon_thumb="icon_thumb"></IconThumb>
        </v-flex>
      </v-layout>
      <v-flex>
        <div v-for="icon_thumb in icon_thumbs">
          <ProductDetails :position="getPosition()" :icon_thumb="icon_thumb" ></ProductDetails>
        </div>
      </v-flex>
    </v-flex>
  </v-layout>
</template>

<script>
  import Hero from '~/components/Hero';
  import IconThumb from '~/components/IconThumb';
  import ProductDetails from '~/components/ProductDetails';

export default {
  components: {
    Hero, IconThumb, ProductDetails
  },
  data() {
    return {
      icon_thumbs: [
        {title: "Modules", icon: 'device_hub', show: false, image: "https://picsum.photos/458/354/?image=420", li: ['First', 'Second', 'Third']},
        {title: "Development Tools", icon: 'desktop_mac', show: false, image: "https://picsum.photos/g/458/354", li: ['First', 'Second', 'Third']},
        {title: "Online Services", icon: "router", show: false, image: "https://picsum.photos/458/354/?image=740", li: ['First', 'Second', 'Third']},
      ],
      position: "left"
    }
  },
  methods: {
    getPosition: function () {
      if (this.position === "left") {
        let position = this.position;
        this.position = "right";
        return position;
      } else {
        let position = this.position;
        this.position = "left";
        return position;
      }
    }
  }
}
</script>

<style>

</style>
