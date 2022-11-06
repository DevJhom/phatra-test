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
    <div class="d-flex flex-column">
      <article-heading :text="heading" class="heading"></article-heading>
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
  margin: 26px 15px 15px 0;
  object-fit: contain;
}

img:hover {
  border-right: 15px solid #594f74;
}

.heading {
  margin: 26px 42px 17px 27px;
}

.heading:hover {
  color: #8272ab;
}

.details {
  margin: 17px 30px 33px 27px;
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
  margin: 0 0 0 27px;
}

a {
  text-decoration: none;
}

@media (max-width: 1200px) {
  img {
    width: 50%;
    height: auto;
    margin: 0;
    object-fit: contain;
    align-self: start;
  }

  .heading {
    margin: 0 8px 8px 8px;
  }

  .details {
    font-size: 0.8rem;
    margin: 0 0 8px 8px;
  }

  .category {
    margin: 0 0 0 8px;
  }
}

@media (max-width: 480px) {
  img {
    width: 200px;
    height: auto;
    margin: 0;
  }

  .heading {
    margin: 0 0 8px 8px;
  }

  .details {
    font-size: 0.5rem;
    margin: 0 0 8px 8px;
  }
  .category {
    margin: 0 0 0 8px;
  }
}
</style>
