<script setup>
const checkout = () => {
  alert("Checkout out items")
}
</script>

<template>
  <div>
    <h1 class="text-4xl">Home</h1>
    <button @click="checkout">Checkout</button>
  </div>
</template>