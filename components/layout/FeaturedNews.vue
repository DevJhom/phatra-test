<script>
import SeeAll from "../ui/SeeAll";
import SetIndex from "../layout/SetIndex";

export default {
  name: "FeaturedNews",
  components: {
    SetIndex,
    SeeAll,
  },
};
</script>

<template>
  <div>
    <div class="d-flex justify-content-between">
      <span class="news">News</span>
      <see-all link="/news" class="me-4"></see-all>
    </div>
    <nuxt-link to="/news/news-Id">
      <img src="@/assets/news/img-news.jpg" alt="news" />
    </nuxt-link>
    <set-index></set-index>
  </div>
</template>

<style scoped>
.news {
  margin: 0 68px 24px 0px;
  font-family: Kanit;
  font-size: 32px;
  font-weight: 500;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.25;
  letter-spacing: normal;
  color: #594f74;
}

@media (max-width: 912px) {
  .news {
    font-size: 1rem;
  }

  img {
    width: 200px;
    height: auto;
  }
}
</style>
