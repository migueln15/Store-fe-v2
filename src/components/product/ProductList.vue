<template>
  <h5>Listado de productos</h5>
  <div class="product-list">
    <div class="product-grid">
      <ProductItem :product="item" v-for="item in products" :key="item.id" />
    </div>
  </div>
</template>

<style>
.product-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 20px;
}
</style>

<script>
import ProductItem from "src/components/product/ProductItem.vue";

export default {
  name: "ProductList",
  components: { ProductItem },
  data() {
    return {
      products: [],
    };
  },
  mounted() {
    this.cargarProductos();
  },
  methods: {
    cargarProductos() {
      let endpointURL = "api/product";
      let token = JSON.parse(localStorage.getItem("userData")).data.token;
      console.log(token);
      let headers = {
        headers: {
          Authorization: "Bearer " + token,
        },
      };

      this.$api
        .get(endpointURL, headers)
        .then((response) => {
          console.log(JSON.stringify(response));
          this.products = response.data;
        })
        .catch((error) => {
          console.log(error);
        });
    },
  },
};
</script>
