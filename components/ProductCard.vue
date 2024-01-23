<!-- ProductCard.vue -->
<template>
  <div class="product-card">
    <div class="product-image">
      <img :src="product.image" :alt="product.name + ' Image'" />
    </div>
    <div class="product-details">
      <h2>{{ product.name }}</h2>
      <p class="description">{{ product.description }}</p>
      <p class="price">{{ product.price }} USD</p>
      <button @click="addToCart(product)">Add to Cart</button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    product: {
      type: Object,
      required: true,
    },
    addToCart: {
      type: Function,
      required: true,
    },
  },
};
</script>

<style scoped>
.product-card {
  display: flex;
  flex-direction: column;
  border: 1px solid #e1e1e1;
  border-radius: 8px;
  overflow: hidden;
  transition: transform 0.2s ease-in-out;
}

.product-card:hover {
  transform: scale(1.05);
}

.product-image img {
  width: 100%;
  height: auto;
}

.product-details {
  padding: 15px;
}

.description {
  color: #555;
}

.price {
  font-weight: bold;
  color: #007BFF;
  margin-bottom: 10px;
}

button {
  background-color: #007BFF;
  color: white;
  padding: 8px 12px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.2s ease-in-out;
}

button:hover {
  background-color: #0056b3;
}
</style>
