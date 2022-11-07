<script>
import ArticleTitle from "../../ui/ArticleTitle";
import SeeAll from "../../ui/SeeAll";
import SetIndex from "./SetIndex";

export default {
  name: "FeaturedNews",
  components: {
    SetIndex,
    SeeAll,
    ArticleTitle,
  },
};
</script>

<template>
  <div class="wrapper">
    <div>
      <div class="d-flex justify-content-between heading-wrapper">
        <article-title text="News"></article-title>
        <see-all link="/news"></see-all>
      </div>
      <nuxt-link to="/news/news1">
        <img src="@/assets/news/img-news.jpg" alt="news" />
      </nuxt-link>
    </div>
    <set-index></set-index>
  </div>
</template>

<style scoped>
* {
  margin: 0;
}

.wrapper {
  display: flex;
  flex-direction: column;
  margin-left: 1rem;
}

.heading-wrapper {
  width: 100%;
}

img {
  margin: 26px 15px 15px 0;
  width: 100%;
}

@media (max-width: 480px) {
  .wrapper {
    flex-direction: row;
    margin: 1rem;
  }

  .heading-wrapper {
    width: 40vw;
  }

  img {
    width: 40vw;
    height: auto;
    margin: 5px 15px 15px 0;
  }
}
</style>
