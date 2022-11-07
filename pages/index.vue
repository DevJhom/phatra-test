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
import SliderComponent from "../components/layout/Landing/SliderComponent";
import NavRectangles from "../components/layout/Landing/NavRectangles";
import Section1 from "../components/layout/Section1/Section1";
import Section2 from "../components/layout/Section2/Section2";

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
  background-image: url(@/assets/bg/bg.png);
  background-size: 100% 100%;
}
</style>
