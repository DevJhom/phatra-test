<script>
import ArticleCategory from "./ArticleCategory.vue";
import ArticleHeading from "./ArticleHeading.vue";

export default {
  name: "CardStyle2",
  props: {
    name: String,
    imgSrc: String,
    heading: String,
    category: String,
    link: String,
  },
  components: {
    ArticleCategory,
    ArticleHeading,
  },
};
</script>

<template>
  <nuxt-link :to="link + ''">
    <div class="wrapper">
      <img :src="imgSrc" :alt="name" />
      <div class="text">
        <article-heading :text="heading" class="heading"></article-heading>
        <article-category :text="category" class="category"></article-category>
      </div>
    </div>
  </nuxt-link>
</template>

<style scoped>
.wrapper {
  display: flex;
  flex-direction: column;
}

img {
  width: 374px;
  height: auto;
  object-fit: contain;
  margin: 33px 27px 29px 2px;
}

.text {
  width: 368px;
}

.category {
  margin-top: 27px;
}

a {
  text-decoration: none;
}

@media (max-width: 912px) {
  .wrapper {
    flex-direction: row;
    margin: 15px 0;
  }

  img {
    width: 200px;
    height: auto;
    margin: 0 8px 0 0;
  }
}
</style>
