<template>
  <div>
    <the-header class="position-absolute"></the-header>
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
