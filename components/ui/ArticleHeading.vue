<script>
export default {
  name: "ArticleHeading",
  props: {
    text: String,
  },
};
</script>

<template>
  <span class="heading">
    {{ text }}
  </span>
</template>

<style scoped>
.heading {
  font-family: Kanit;
  font-size: 1.5rem;
  font-weight: 500;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.25;
  letter-spacing: normal;
  color: #594f74;
}

@media (max-width: 912px) {
  .heading {
    font-size: 0.7rem;
  }
}
</style>
