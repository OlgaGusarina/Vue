<template>
  <div class="home">
    <img alt="I'm in" src="../assets/imin.jpg" />
    <Calculator />
  </div>
</template>

<script>
// @ is an alias to /src
import Calculator from "@/components/calculator.vue";

export default {
  name: "Home",
  components: {
    Calculator,
  },
};
</script>

<style>
img {
  height: 160px;
}
</style>
