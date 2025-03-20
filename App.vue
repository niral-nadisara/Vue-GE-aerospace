<template>
  <div id="app">
    <!-- Step 3: Add a heading -->
    <h1>Compute Product</h1>

    <!-- Step 4: Embed an image -->
    <img
      src="https://platform.vox.com/wp-content/uploads/sites/2/chorus/uploads/chorus_asset/file/19397812/1048232144.jpg.jpg?quality=90&strip=all&crop=0%2C0.0044935741889063%2C100%2C99.991012851622&w=1440$0"
      alt="Example Image"
      width="200"
    />

    <!-- Step 5: Add variables for two numbers -->
    <div>
      <p>Number 1: {{ number1 }}</p>
      <p>Number 2: {{ number2 }}</p>
    </div>

    <!-- Step 6: Add a compute button -->
    <button v-if="!computed" @click="computeProduct">Compute</button>

    <!-- Step 7: Display the product when computed -->
    <div v-if="computed">
      <p>The product of {{ number1 }} and {{ number2 }} is: {{ product }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      number1: 5, // Set your first number here
      number2: 10, // Set your second number here
      computed: false, // Tracks if the product has been computed
      product: null, // Stores the computed product
    };
  },
  methods: {
    computeProduct() {
      // Calculate the product
      this.product = this.number1 * this.number2;
      // Hide the button and show the result
      this.computed = true;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  margin-top: 60px;
}

img {
  margin: 20px 0;
}

button {
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
}
</style>