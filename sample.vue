// Make sure you have installed: npm install -g @vue/cli-service-global
// To run: vue serve sample.vue

<template>
  <div>
    <h2>{{name}}</h2>
    <p>{{city}}</p>
    <hr />
    <p :class="style">This is a sample text with dynamic styling</p>
    <button @click="changeStyle">Change Style</button>
  </div>
</template>

<script>
export default {
  name: "sample",
  data() {
    return {
      name: "Vinayak",
      city: "Hyderabad",
      style: null,
      index: 0,
      styleArray: [
        {
          active: true,
          paid: false
        },
        {
          active: false,
          paid: true
        },
        {
          active: true,
          paid: true
        }
      ]
    };
  },
  methods: {
    changeStyle() {
      ++this.index;
      if (this.index === 3) {
        this.index = 0;
      }

      this.style = this.styleArray[this.index];
    }
  }
};
</script>

<style scoped>
h2 {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-size: 30px;
  color: blue;
}

p {
  font-size: 14px;
  color: brown;
}

.active {
  color: green;
  font-size: 24px;
  font-family: "Courier New", Courier, monospace;
}

.paid {
  font-style: italic;
  text-decoration: underline;
}
</style>