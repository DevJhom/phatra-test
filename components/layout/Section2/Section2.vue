<script>
import CardStyle3 from "../../ui/CardStyle3.vue";
import FeaturedClips from "./FeaturedClips.vue";

export default {
  components: {
    CardStyle3,
    FeaturedClips,
  },
  data() {
    return {
      active: "KKP Focus",
    };
  },
  methods: {
    clickHandler(e) {
      this.active = e.target.outerText;
      console.log(this.active);
    },
  },
};
</script>

<template>
  <div class="container">
    <div class="d-flex mt-3">
      <div class="line"></div>
      <span class="kkp-channel">KKP Channel</span>
      <span class="kkp-channel-text">
        อัปเดตทุกความรู้ด้านการเงินและการลงทุนก่อนใคร
        พร้อมอินเทรนด์ไปกับหลากหลายเรื่องราวไลฟ์สไตล์
      </span>
    </div>
    <div class="d-flex kkp-box">
      <span
        class="clip-heading"
        :class="active === 'KKP Focus' ? 'active' : ''"
        @click="clickHandler"
        >KKP Focus</span
      >
      <div class="v-line"></div>
      <span
        class="clip-heading"
        :class="active === 'OPTIMISE' ? 'active' : ''"
        @click="clickHandler"
        >OPTIMISE</span
      >
      <div class="v-line"></div>
      <span
        class="clip-heading"
        :class="active === 'KKP Advisor' ? 'active' : ''"
        @click="clickHandler"
        >KKP Advisor</span
      >
      <div class="v-line"></div>
    </div>
    <div class="d-flex ms-4">
      <iframe
        src="https://www.youtube.com/embed/gFLaIDEbJHc"
        title="KKP Focus"
      >
      </iframe>
      <div class="d-flex flex-column ms-2 my-auto">
        <div class="long-line"></div>
        <span class="kkp-focus">{{ active }}</span>
        <span class="kkp-focus-text">
          ฝนนักสู้ พบเรื่องราวจริง เจ็บจริง ประสบความสำเร็จจริง
          ที่จะเป็นแรงกระตุ้นให้ SME นักสู้รุ่นต่อไป ได้ก้าวไปถึงฝัน
        </span>
        <div class="long-line"></div>
      </div>
    </div>

    <featured-clips></featured-clips>
  </div>
</template>

<style scoped>
* {
  font-stretch: normal;
  font-style: normal;
}

.line {
  width: 52px;
  height: 2px;
  margin: 63px 18px 86px 0px;
  border-style: solid;
  border-width: 2px;
  border-image-source: linear-gradient(to right, #e9eaef -18%, #b9b9c3 122%);
  border-image-slice: 1;
}

.kkp-channel {
  margin: 43px 33px 69px 18px;
  font-family: Kanit;
  font-size: 32px;
  font-weight: 500;
  line-height: 1.25;
  letter-spacing: normal;
  color: #594f74;
}

.kkp-channel-text {
  margin: 55px 125px 71px 26px;
  font-family: Kanit;
  font-size: 18px;
  font-weight: normal;
  line-height: 1.44;
  letter-spacing: normal;
  color: #84848f;
}

.kkp-box {
  margin: 3rem 2rem;
}

.clip-heading {
  height: 30px;
  margin: 3px 33px 2px 0;
  font-family: Kanit;
  font-size: 24px;
  font-weight: 500;
  line-height: 1.25;
  letter-spacing: normal;
  color: #84848f;
}

.active {
  color: #594f74;
}

.v-line {
  height: 23px;
  margin: 5px 43px 7px 33px;
  border: solid 1px #adacb9;
}

iframe {
  width: 60%;
  height: 450px;
}

.long-line {
  width: 266px;
  height: 2px;
  margin: 2rem 2rem;
  border-style: solid;
  border-width: 2px;
  border-image-source: linear-gradient(
    to right,
    #d0cfd8 -3%,
    #e9eaef 55%,
    #b9b9c3 111%
  );
  border-image-slice: 1;
}

.kkp-focus {
  margin-left: 2rem;
  font-family: Kanit;
  font-size: 42px;
  font-weight: 500;
  line-height: normal;
  letter-spacing: normal;
  color: #594f74;
}

.kkp-focus-text {
  width: 276px;
  margin-left: 2rem;
  font-family: Kanit;
  font-size: 20px;
  font-weight: normal;
  line-height: 1.4;
  letter-spacing: normal;
  color: #84848f;
}

@media (max-width: 912px) {
  .line {
    margin: 5px;
  }

  .kkp-channel {
    font-size: 0.75rem;
    width: 120px;
    margin: 0 5px;
  }

  .kkp-channel-text {
    font-size: 0.5rem;
    margin: 0;
  }

  .kkp-box {
    margin: 1rem 0.5rem;
  }

  .clip-heading {
    font-size: 0.5rem;
    height: 0.5rem;
    margin: 0;
  }

  .v-line {
    height: 0.5rem;
    margin: 0 5px;
  }

  iframe {
    width: 50%;
    height: 200px;
    margin: 0;
  }

  .long-line {
    width: 100px;
    height: 1px;
    margin: 5px 0 0 5px;
  }

  .kkp-focus {
    font-size: 10px;
    margin: 10px 0 0 5px;
  }

  .kkp-focus-text {
    width: 100px;
    font-size: 7px;
    margin: 10px 0 5px 5px;
  }
}
</style>
