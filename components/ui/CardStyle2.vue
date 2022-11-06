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
      <div class="text-wrapper">
        <article-heading :text="heading"></article-heading>
        <article-category :text="category" class="category"></article-category>
      </div>
    </div>
  </nuxt-link>
</template>

<style scoped>
.wrapper {
  display: flex;
  flex-direction: column;
  margin-right: 0.8rem;
}

img {
  width: 20vw;
  height: auto;
  object-fit: contain;
  margin: 33px 27px 29px 2px;
}

img:hover {
  border-right: 15px solid #594f74;
}

.text-wrapper{
  width: 100%;
}

.category {
  margin-top: 27px;
}

a {
  text-decoration: none;
}

@media (max-width: 912px) {
  img {
    margin: 33px 0 0 0;
  }
}

@media (max-width: 480px) {
  .wrapper {
    flex-direction: row;
  }

  .category {
    margin-top: 5px;
  }

  img {
    width: 200px;
    height: auto;
    margin: 8px 8px 0 0;
  }
}
</style>
