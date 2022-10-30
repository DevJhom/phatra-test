<script>
import ArticleHeading from "./ArticleHeading.vue";

export default {
  name: "CardStyle3",
  props: {
    name: String,
    imgSrc: String,
    description: String,
    link: String,
  },
  components: {
    ArticleHeading,
  },
};
</script>

<template>
  <nuxt-link :to="link + ''">
    <div class="wrapper">
      <img :src="imgSrc" :alt="name" />
      <article-heading :text="description" class="description"></article-heading>
    </div>
  </nuxt-link>
</template>

<style scoped>
.wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
}

img {
  width: 362px;
  height: 208px;
}

.description {
  width: 362px;
  margin: 24px 0;
}

a {
  text-decoration: none;
}

@media (max-width: 912px) {
  img {
    width: 200px;
    height: auto;
    margin: 5px 0;
  }

  .wrapper {
    flex-direction: row;
  }

  .description {
  margin: 0 0 0 5px;
}
}
</style>
