<script>
import CardStyle1 from "../../ui/CardStyle1";
import CardStyle2 from "../../ui/CardStyle2";
import ArticleTitle from "../../ui/ArticleTitle";
import SeeAll from "../../ui/SeeAll";

import image1 from "@/assets/articles/article-1/img-article-1.jpg";
import image2 from "@/assets/articles/article-2/img-article-2.jpg";
import image3 from "@/assets/articles/article-3/img-article-3.jpg";

export default {
  components: {
    CardStyle1,
    CardStyle2,
    SeeAll,
    ArticleTitle,
  },
  data() {
    return {
      image1,
      image2,
      image3,
      articles: [
        {
          id: "1",
          heading:
            "Margin of Safety กลยุทธ์การลงทุนอย่างปลอดภัย หลักการลงทุนของเบนจามิน เกรแฮม",
          details:
            "ตอบคำถามที่ว่า คุณมีความจำเป็น พร้อมเป็นเจ้าของหรือยัง เช่น เพื่อหน้าที่การงาน อาชีพ หรือการเดินทาง ความสะดวกสบาย เพราะการซื้อรถนอกจากค่ารถแล้ว ยังมีค่าน้ำมัน ค่าบำรุงรักษา ค่าประกันภัย ซึ่งเป็นค่าใช้จ่ายในระยะยาว",
          category: "การลงทุน",
          imageUrl: image1,
        },
        {
          id: "2",
          heading: "จับจังหวะการลงทุนเป็นก็สร้างเงินล้านได้ง่ายๆใกล้แค่เอื้อม",
          details: "",
          category: "การลงทุน",
          imageUrl: image2,
        },
        {
          id: "3",
          heading:
            "Margin of Safety กลยุทธ์การลงทุนอย่างปลอดภัย Margin of Safety",
          details: "",
          category: "การลงทุน",
          imageUrl: image3,
        },
      ],
    };
  },
};
</script>

<template>
  <div>
    <div class="d-flex justify-content-between">
      <article-title text="Article" class="article-title"></article-title>
      <see-all class="me-3" link="/articles"></see-all>
    </div>
    <card-style-1
      class="d-flex"
      :name="articles[0].id"
      :heading="articles[0].heading"
      :details="articles[0].details"
      :category="articles[0].category"
      :imgSrc="articles[0].imageUrl"
      :link="'/articles/article' + articles[0].id"
    ></card-style-1>
    <div class="wrapper">
      <card-style-2
        class="card-style-2"
        v-for="article in articles.slice(1)"
        :key="article.id"
        :name="article.id"
        :heading="article.heading"
        :category="article.category"
        :imgSrc="article.imageUrl"
        :link="'/articles/article' + article.id"
      ></card-style-2>
    </div>
  </div>
</template>

<style scoped>
.wrapper {
  display: flex;
}

.card-style-2 {
  width: 50%;
}

@media (max-width: 480px) {
  .article-text {
    font-size: 1rem;
  }

  .wrapper {
    flex-direction: column;
  }

  .card-style-2 {
    width: 100%;
  }
}
</style>
