<script>
import SeeAll from "../ui/SeeAll";
import CardStyle3 from "../ui/CardStyle3";

import clip1 from "@/assets/clips/clip-1/clip-1.jpg";
import clip2 from "@/assets/clips/clip-2/clip-2.jpg";
import clip3 from "@/assets/clips/clip-3/clip-3.jpg";

export default {
  components: {
    CardStyle3,
    SeeAll,
  },
  data() {
    return {
      clip1,
      clip2,
      clip3,
      clips: [
        {
          id: "1",
          description: "KKP Focus ช่วงที่ 2 กูรู... โต๊ะกลม",
          imageUrl: clip1,
        },
        {
          id: "2",
          description: "KKP Focus ช่วงที่ 1 ย่อประเด็นโลก โยกประเด็นร้อน",
          imageUrl: clip2,
        },
        {
          id: "3",
          description: "KKP Focus ช่วงที่ 2 กูรู... โต๊ะกลม",
          imageUrl: clip3,
        },
      ],
    };
  },
};
</script>

<template>
  <div class="mb-5">
    <see-all class="d-flex justify-content-end my-3" link="/clips"></see-all>
    <div class="wrapper">
      <card-style-3
        v-for="clip in clips"
        :key="clip.id"
        :name="clip.id"
        :description="clip.description"
        :imgSrc="clip.imageUrl"
        :link="'/clips/clip' + clip.id"
      ></card-style-3>
    </div>
  </div>
</template>

<style scoped>
.wrapper {
  display: flex;
  justify-content: space-between;
}

@media (max-width: 912px) {
  .wrapper {
    flex-direction: column;
  }

  img {
    width: 200px;
    height: 200px;
  }
}
</style>
