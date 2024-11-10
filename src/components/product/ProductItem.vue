<template>
  <q-card class="product-card">
    <q-card-section>
      <q-img :src="product.imageUrl" alt="Imagen del producto" />
    </q-card-section>
    <q-card-section>
      <q-card-title>{{ product.description }}</q-card-title>
      <div class="text-h6 font-weight-bold">{{ product.price }}</div>
      <div class="text-center">
        <q-btn color="primary" label="Agregar"></q-btn>
      </div>
    </q-card-section>
  </q-card>
</template>

<style>
.product-card {
  width: 300px;
}
.product-card q-card-section {
  height: 100px;
  overflow: hidden;
}
</style>

<script>
export default {
  name: "ProductItem",
  data() {
    return {
      urlImage:
        "https://cdn-dynmedia-1.microsoft.com/is/image/microsoftcorp/Surface-Laptop-Go-3_OG_Twitter-image?scl=1",
    };
  },
  props: {
    product: {
      type: Object,
      Required: true,
    },
  },
};
</script>
