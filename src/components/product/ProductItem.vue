<template>
  <q-card class="product-card">
    <q-card-section>
      <q-img :src="urlImage" alt="Imagen del producto" />
    </q-card-section>
  </q-card>
</template>

<style></style>

<script>
export default {
  name: "ProductItem",
  data() {
    return {
      urlImage:
        "https://cdn-dynmedia-1.microsoft.com/is/image/microsoftcorp/Surface-Laptop-Go-3_OG_Twitter-image?scl=1",
    };
  },
};
</script>
