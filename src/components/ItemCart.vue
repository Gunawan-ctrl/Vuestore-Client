<template>
  <div class="product-container">
    <img
      :src="`https://vuestore-api.vercel.app${item.imageUrl}`"
      class="product-image"
    />
    <div class="details-wrap">
      <h3>{{ item.name }}</h3>
      <p>Rp {{ item.price }}</p>
    </div>
    <button @click="$emit('remove-item', item.code)" class="remove-button">
      Remove
    </button>
  </div>
</template>

<script>
export default {
  props: ["item"],
};
</script>

<style scoped>
.product-container {
  align-content: "center";
  border-bottom: 1px solid #ddd;
  display: flex;
  padding: 16px;
  width: 100%;
}
.product-image {
  flex: 1;
  height: 100px;
  max-width: 100px;
}
.details-wrap {
  padding: 0 16px;
  flex: 3;
}
.remove-button {
  flex: 1;
  margin: auto;
}
</style>
