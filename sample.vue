// Make sure you have installed: npm install -g @vue/cli-service-global
// To run: vue serve sample.vue

<template>
  <div>
    <h2>{{name}}</h2>
    <p>{{city}}</p>
    <button @click="sayHello">Click</button>
  </div>
</template>

<script>
export default {
  name: "sample",
  data() {
    return {
      name: "Vinayak",
      city: "Hyderabad"
    };
  },
  methods: {
    sayHello() {
      alert(`${this.name} says hello to you all!`);
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
</style>