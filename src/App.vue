<template>
  <product msg="data is here" />
  <travelHome msg="data is here" />
  <RegForm msg="data is here" />
  <!-- <Home msg="i am from Home components" /> -->
</template>

<script>
import product from "./components/ProductApi.vue";
import RegForm from "./components/RegForm.vue";
import Home from "./components/Home.vue";
// import travelHome from "./components/TravelHome.vue";

export default {
  name: "App",

  components: { Home, product, RegForm },
  data() {
    return {};
  },
};
</script>
