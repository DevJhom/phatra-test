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
    <iframe
      frameborder="0"
      scrolling="no"
      width="200"
      height="206"
      src="http://www.settrade.com/banner/banner3.jsp"
    ></iframe>
    <!-- <iframe
      frameborder="0"
      scrolling="no"
      width="200"
      height="260"
      src="https://weblink.settrade.com/banner/banner3.jsp"
    ></iframe> -->
  </div>
</template>

<style scoped>
.component-wrapper {
  margin: 36px 0 0 0px;
  padding: 10px 32px 21px 43px;
  background-color: #fff;
  width: 80%;
}

iframe {
  margin: 8px 0 0 6px;
  object-fit: contain;
  align-self: center;
}

@media (max-width: 912px) {
  .component-wrapper {
    margin: 0;
    padding: 0;
  }

  iframe {
    width: 150px;
    height: auto;
    margin: 0;
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

  iframe {
    width: 150px;
    height: auto;
    margin: 0;
  }
}
</style>
