<script>
import CardStyle1 from "../ui/CardStyle1";
import CardStyle2 from "../ui/CardStyle2";
import SeeAll from "../ui/SeeAll";

import image1 from "@/assets/articles/article-1/img-article-1.jpg";
import image2 from "@/assets/articles/article-2/img-article-2.jpg";
import image3 from "@/assets/articles/article-3/img-article-3.jpg";

export default {
  components: {
    CardStyle1,
    CardStyle2,
    SeeAll,
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
      <span class="article-text">Article</span>
      <see-all link="/articles" class="me-4"></see-all>
    </div>
    <card-style-1
      class="d-flex"
      :name="articles[0].id"
      :heading="articles[0].heading"
      :details="articles[0].details"
      :category="articles[0].category"
      :imgSrc="articles[0].imageUrl"
      link="/articles/article-Id"
    ></card-style-1>
    <div class="wrapper">
      <card-style-2
        v-for="article in articles.slice(1)"
        :key="article.id"
        :name="article.id"
        :heading="article.heading"
        :category="article.category"
        :imgSrc="article.imageUrl"
        :link="'/articles/article-Id'"
      ></card-style-2>
    </div>
  </div>
</template>

<style scoped>
.article-text {
  font-family: Kanit;
  font-size: 2rem;
  font-weight: 500;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.25;
  letter-spacing: normal;
  color: #594f74;
}

.wrapper {
  display: flex;
}

@media (max-width: 912px) {
  .article-text {
    font-size: 1rem;
  }

  .wrapper {
    flex-direction: column;
  }
}
</style>
