<template>
  <div>
    <the-header class="header"></the-header>
    <Nuxt />
    <the-footer></the-footer>
  </div>
</template>

<script>
import TheHeader from "../components/layout/TheHeader";
import TheFooter from "../components/layout/TheFooter";

export default {
  components: {
    TheHeader,
    TheFooter,
  },
};
</script>

<style scoped>
.header {
  background-color: #21201A;
}
</style>
