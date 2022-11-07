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
  <div class="component-wrapper">
    <article-title text="Set Index" class="title"></article-title>
    <iframe
      src="https://weblink.settrade.com/banner/banner3.jsp"
      width="200"
      height="260"
      frameborder="0"
      scrolling="no"
    ></iframe>
  </div>
</template>

<style scoped>
.component-wrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
  width: 100%;
  height: 300px;
  margin-top: 3rem;
  padding: 1rem;
  background-color: #fff;
}

.title {
  font-size: 1.5rem;
  margin: 0 0 1rem 3rem;
}

iframe {
  object-fit: contain;
  align-self: center;
}

@media (max-width: 912px) {
  .component-wrapper {
    padding: 5px;
    height: 200px;
  }

  .title {
    font-size: 1rem;
    margin: 5px 0;
  }

  iframe {
    width: 150px;
    height: 150px;
  }
}

@media (max-width: 480px) {
  .component-wrapper {
    margin: 0;
    padding: 15px;
    height: 120px;
  }

  iframe {
    width: 100px;
    height: 100px;
  }

  .title {
    margin: 0;
    font-size: 1rem;
  }
}
</style>
