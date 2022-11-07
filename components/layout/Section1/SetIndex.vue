<script>
import ArticleTitle from "../../ui/ArticleTitle";

export default {
  name: "SetIndex",
  components: {
    ArticleTitle,
  },
};
</script>

<template>
  <div class="component-wrapper d-flex flex-column">
    <article-title text="Set Index" class="article-title"></article-title>
    <!-- <iframe
      frameborder="0"
      scrolling="no"
      width="200"
      height="206"
      src="http://www.settrade.com/banner/banner3.jsp"
    ></iframe> -->
    <iframe
      frameborder="0"
      scrolling="no"
      width="200"
      height="260"
      src="https://weblink.settrade.com/banner/banner3.jsp"
    ></iframe>
  </div>
</template>

<style scoped>
.component-wrapper {
  width: 100%;
  margin-top: 36px;
  padding: 2rem;
  background-color: #fff;
}

iframe {
  width: 100%;
  height: 100%;
  margin: 8px 0 0 6px;
  object-fit: contain;
  align-self: center;
}

@media (max-width: 912px) {
  .component-wrapper {
    margin: 0;
    padding: 1rem;
  }
}

@media (max-width: 480px) {
  .component-wrapper {
    margin: 0;
    padding: 15px;
  }

  .title {
    margin: 0;
    font-size: 1rem;
  }
}
</style>
