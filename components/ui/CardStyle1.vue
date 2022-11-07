<script>
import ArticleCategory from "./ArticleCategory.vue";
import ArticleHeading from "./ArticleHeading.vue";

export default {
  name: "CardStyle1",
  props: {
    name: String,
    imgSrc: String,
    heading: String,
    details: String,
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
    <img :src="imgSrc" :alt="name" />
    <div class="d-flex flex-column text-wrapper">
      <article-heading :text="heading"></article-heading>
      <small class="details">
        {{ details }}
      </small>
      <div class="d-flex">
        <article-category :text="category" class="category" />
      </div>
    </div>
  </nuxt-link>
</template>

<style scoped>
img {
  width: 60%;
  height: auto;
  margin: 26px 0 15px 0;
  object-fit: contain;
  align-self: start;
}

img:hover {
  border-right: 15px solid #594f74;
}

.text-wrapper {
  width: 40%;
  margin: 26px 0 0 26px;
}

.details {
  font-family: Tahoma;
  font-size: 1rem;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.5;
  letter-spacing: normal;
  color: #84848f;
}

.category {
  margin-top: 26px;
}

a {
  text-decoration: none;
}

@media (max-width: 999px) {
  img {
    width: 50%;
  }

  .text-wrapper {
    width: 50%;
    margin: 26px 0 0 8px;
  }

  .details {
    font-size: 0.6rem;
  }

  .category {
    margin-top: 8px;
  }
}

@media (max-width: 480px) {
  img {
    width: 200px;
  }

  .details {
    font-size: 0.5rem;
  }

  .category {
    margin-top: 8px;
  }
}

@media (max-width: 320px) {
  .details {
    display: none;
  }
}
</style>
