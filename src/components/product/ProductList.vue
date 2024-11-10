<template>
  <h5>Listado de productos</h5>
  <div class="product-list">
    <div class="product-grid">
      <div class="product-item">
        <ProductItem />
      </div>
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
};
</script>
