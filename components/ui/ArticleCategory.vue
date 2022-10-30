<script>
export default {
  name: "ArticleCategory",
  props: {
    text: String,
  },
};
</script>

<template>
  <div class="d-flex">
    <div class="line"></div>
    <span class="category">
      {{ text }}
    </span>
  </div>
</template>

<style scoped>

.category {
  height: 17px;
  font-family: Tahoma;
  font-size: 0.875rem;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1;
  letter-spacing: normal;
  color: #635f98;
}

.line {
  margin-right: 10px;
  width: 3px;
  height: 15px;
  background-color: #635f98;
}

@media (max-width: 912px) {
.category {
    font-size: 0.5rem;
}

.line {
  width: 2px;
  height: 10px;
  background-color: #635f98;
}
}

</style>
