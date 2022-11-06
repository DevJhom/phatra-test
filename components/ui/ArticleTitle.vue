<script>
export default {
  name: "ArticleTitle",
  props: {
    text: String,
  },
};
</script>

<template>
  <span>
    {{ text }}
  </span>
</template>

<style scoped>
span {
  font-family: Kanit;
  font-size: 2rem;
  font-weight: 500;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.25;
  letter-spacing: normal;
  color: #594f74;
}

@media (max-width: 1024px) {
  span {
    font-size: 1.2rem;
  }
}

@media (max-width: 480px) {
  span {
    font-size: 0.8rem;
  }
}
</style>
