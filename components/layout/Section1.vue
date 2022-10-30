<script>
import FeaturedArticles from "../layout/FeaturedArticles";
import FeaturedNews from "../layout/FeaturedNews";

export default {
  components: {
    FeaturedArticles,
    FeaturedNews,
  },
};
</script>

<template>
  <div class="container wrapper">
    <featured-articles class="featured-articles"></featured-articles>
    <div class="featured-news">
      <featured-news></featured-news>
    </div>
  </div>
</template>

<style scoped>
.wrapper {
  display: flex;
  width: 100vw;
  margin-top: 100px;
  padding-bottom: 150px;
}

.featured-articles {
  width: 70%;
}

.featured-news {
  width: 30%;
}

@media (max-width: 912px) {
  .wrapper {
    flex-direction: column;
    margin-top: 20px;
  }

  .featured-articles {
    width: 100%;
  }

  .featured-news {
    width: 100%;
  }
}
</style>
