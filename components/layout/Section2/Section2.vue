<script>
import KkpVideo from "./KkpVideo.vue"
import CardStyle3 from "../../ui/CardStyle3.vue";
import FeaturedClips from "./FeaturedClips.vue";

export default {
  components: {
    KkpVideo,
    CardStyle3,
    FeaturedClips,
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
    <kkp-video class="kkp-video"></kkp-video>
    <featured-clips></featured-clips>
  </div>
</template>

<style scoped>
* {
  font-stretch: normal;
  font-style: normal;
  letter-spacing: normal;
}

.line {
  width: 52px;
  height: 2px;
  border-style: solid;
  border-width: 2px;
  border-image-source: linear-gradient(to right, #e9eaef -18%, #b9b9c3 122%);
  border-image-slice: 1;
  margin: auto 0;
}

.kkp-channel {
  font-family: Kanit;
  font-size: 32px;
  font-weight: 500;
  line-height: 1.25;
  color: #594f74;
  margin: auto 1.5rem;
}

.kkp-channel-text {
  font-family: Kanit;
  font-size: 18px;
  font-weight: normal;
  line-height: 1.44;
  color: #84848f;
  margin: auto 0;
}

.kkp-video {
  margin: 3rem 0;
}

@media (max-width: 480px) {
  .line {
    margin: 5px;
  }

  .kkp-channel {
    font-size: 0.75rem;
  }

  .kkp-channel-text {
    font-size: 0.5rem;
  }
}
</style>
