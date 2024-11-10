<template>
  <h6>Filtros</h6>
  <div class="category-filter">
    <label>Categoría</label>
    <q-select label="Categoría" v-model="model" :options="categories" />
  </div>
  <div class="price-filter">
    <label>Rango de precios</label>
    <q-input v-model="pMinimo" class="precios" type="number" label="Míximo" />
    <q-input v-model="pMaximo" class="precios" type="number" label="Máximo" />
  </div>
</template>

<style></style>

<script>
export default {
  name: "ProductFilter",
  data() {
    return {
      pMinimo: 0,
      pMaximo: 0,
      model: null,
      categories: ["Celulares", "Televisores", "Laptop"],
    };
  },
};
</script>
