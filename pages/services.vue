<template>
    <div class="mt-4">
        <v-layout  lign-start justify-center row fill-height >
            <v-flex  xs11 sm11 md10 >
                <v-flex style="margin-bottom: 100px">
                    <div v-for="icon_thumb in icon_thumbs">
                        <ProductDetails :position="getPosition()" :icon_thumb="icon_thumb" ></ProductDetails>
                    </div>
                </v-flex>
            </v-flex>
        </v-layout>
    </div>
</template>

<script>
    import ProductDetails from "../components/ProductDetails";

    export default {
		    name: "services",
	      components: {ProductDetails},
	      data() {
		        return {
            icon_thumbs: [
              {title: "Service 1", icon: 'device_hub', show: 'false', image: "https://picsum.photos/458/354/?image=420"},
              {title: "Service 2", icon: 'desktop_mac', show: 'false', image: "https://picsum.photos/g/458/354"},
              {title: "Service 3", icon: "router", show: 'false', image: "https://picsum.photos/458/354/?image=740"},
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
    };
</script>

<style scoped>

</style>