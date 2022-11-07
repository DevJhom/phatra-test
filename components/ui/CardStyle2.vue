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
  margin: 2rem 0.8rem 0 0;
}

img {
  width: 95%;
  height: auto;
  object-fit: contain;
}

img:hover {
  border-right: 15px solid #594f74;
}

.text-wrapper {
  display: flex;
  flex-direction: column;
  width: 95%;
  margin-top: 26px;
}

.category {
  margin-top: 27px;
}

a {
  text-decoration: none;
}

@media (max-width: 912px) {
  .wrapper {
    margin: 1rem 0.2rem 0 0;
  }

  .text-wrapper {
    margin: 8px;
  }

  .category {
    margin-top: 8px;
  }
}

@media (max-width: 480px) {
  .wrapper {
    flex-direction: row;
  }

  .text-wrapper {
    margin-top: 0;
    margin-left: 8px;
  }

  .category {
    margin-top: 5px;
  }

  img {
    width: 200px;
  }
}
</style>
