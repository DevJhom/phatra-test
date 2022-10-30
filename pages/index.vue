<template>
  <div>
    <slider-component></slider-component>
    <div class="bg">
      <nav-rectangles></nav-rectangles>
      <section-1></section-1>
    </div>
    <section-2></section-2>
  </div>
</template>

<script>
import SliderComponent from "../components/layout/SliderComponent";
import NavRectangles from "../components/layout/NavRectangles";
import Section1 from "../components/layout/Section1";
import Section2 from "../components/layout/Section2";

export default {
  layout: "home",
  components: {
    SliderComponent,
    NavRectangles,
    Section1,
    Section2,
  },
};
</script>

<style scoped>
.bg {
  width: 100vw;
  background-image: url(@/assets/bg/bg.png);
  background-size: cover;
}
</style>
