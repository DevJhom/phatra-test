<script>
import FeaturedArticles from "./FeaturedArticles";
import FeaturedNews from "./FeaturedNews";

export default {
  components: {
    FeaturedArticles,
    FeaturedNews,
  },
};
</script>

<template>
  <div class="container component-wrapper">
    <featured-articles class="featured-articles"></featured-articles>
    <div class="featured-news">
      <featured-news></featured-news>
    </div>
  </div>
</template>

<style scoped>
.component-wrapper {
  display: flex;
  width: 100%;
  margin-top: 100px;
  padding-bottom: 150px;
}

.featured-articles {
  width: 70%;
}

.featured-news {
  width: 30%;
}

@media (max-width: 480px) {
  .component-wrapper {
    flex-direction: column;
    margin-top: 20px;
    padding-bottom: 50px;
  }

  .featured-articles {
    width: 100%;
  }

  .featured-news {
    width: 100%;
  }
}
</style>
