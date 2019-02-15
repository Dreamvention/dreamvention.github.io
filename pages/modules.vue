<template>
    <v-layout justify-center>
        <v-flex xs12 sm12 md11 lg10 xl10 >
            <Search title="Dreamvention Free Modules" @search='onSearch'></Search>
            <div class="product-thumb">
                <v-layout row wrap>
                    <v-flex xs6 sm6 md4 lg3 xl3 v-for="product_thumb in result_product_thumbs">
                        <ProductThumb :product_thumb="product_thumb"></ProductThumb>
                    </v-flex>
                    <v-alert :value="true"
                             color="error"
                             icon="warning"
                             outline
                             v-show="empty">
                        No results found for your request
                    </v-alert>
                </v-layout>
            </div>
        </v-flex>
    </v-layout>
</template>

<script>
	import ProductThumb from '~/components/ProductThumb';
	import Search from "~/components/Search";

	export default {
		name: "modules",
		components: {Search, ProductThumb},
		data() {
			return {
				product_thumbs: [
					{title: "Frontend Toolbar", src: "https://image.opencart.com/cache/5941392625a97-resize-710x380.jpg", git_link: 'https://www.google.com'},
					{title: "Shopunity", src: "https://image.opencart.com/cache/5a097cf16318f-resize-710x380.jpg", git_link: ''},
					{title: "Export Import", src: "https://image.opencart.com/cache/59b938b00cbfb-resize-710x380.jpg", git_link: ''},
					{title: "Export Import", src: "https://image.opencart.com/cache/59b938b00cbfb-resize-710x380.jpg", git_link: ''},
					{title: "Shopunity", src: "https://image.opencart.com/cache/5a097cf16318f-resize-710x380.jpg", git_link: ''},
					{title: "Export Import", src: "https://image.opencart.com/cache/59b938b00cbfb-resize-710x380.jpg", git_link: ''},
					{title: "Frontend Toolbar", src: "https://image.opencart.com/cache/5941392625a97-resize-710x380.jpg", git_link: ''},
					{title: "Shopunity", src: "https://image.opencart.com/cache/5a097cf16318f-resize-710x380.jpg", git_link: ''},
					{title: "Frontend Toolbar", src: "https://image.opencart.com/cache/5941392625a97-resize-710x380.jpg", git_link: ''},
					{title: "Export Import", src: "https://image.opencart.com/cache/59b938b00cbfb-resize-710x380.jpg", git_link: ''},
					{title: "Shopunity", src: "https://image.opencart.com/cache/5a097cf16318f-resize-710x380.jpg", git_link: ''},
					{title: "Export Import", src: "https://image.opencart.com/cache/59b938b00cbfb-resize-710x380.jpg", git_link: ''},
					{title: "Frontend Toolbar", src: "https://image.opencart.com/cache/5941392625a97-resize-710x380.jpg", git_link: ''},
					{title: "Shopunity", src: "https://image.opencart.com/cache/5a097cf16318f-resize-710x380.jpg", git_link: ''},
					{title: "Export Import", src: "https://image.opencart.com/cache/59b938b00cbfb-resize-710x380.jpg", git_link: ''},
					{title: "Frontend Toolbar", src: "https://image.opencart.com/cache/5941392625a97-resize-710x380.jpg", git_link: ''},
					{title: "Shopunity", src: "https://image.opencart.com/cache/5a097cf16318f-resize-710x380.jpg", git_link: ''},
					{title: "Frontend Toolbar", src: "https://image.opencart.com/cache/5941392625a97-resize-710x380.jpg", git_link: ''},
					{title: "Shopunity", src: "https://image.opencart.com/cache/5a097cf16318f-resize-710x380.jpg", git_link: ''},
					{title: "Export Import", src: "https://image.opencart.com/cache/59b938b00cbfb-resize-710x380.jpg", git_link: ''},
				],
				search: '',
				empty: false,
			}
		},
		computed: {
			result_product_thumbs: function () {
				if (this.search === '') {
					this.empty = false;
					return this.product_thumbs;
				} else {
					this.empty = false;
					var search_pattern = new RegExp(this.search, 'i');
					var res_mas = [];
					for (var i = 0; i < this.product_thumbs.length; i++) {
						if (search_pattern.test(this.product_thumbs[i].title) === true) {
							res_mas.push(this.product_thumbs[i]);
						}
					}
					if (res_mas.length === 0) {
			  console.log(res_mas.length);
						this.empty = true;
					}
					return res_mas;
				}
			}
		},
		methods: {
			onSearch(data) {
				this.search = data.search;
			}
		}
	};
</script>

<style scoped>
    .product-thumb {
        margin-top: 50px;
    }
</style>