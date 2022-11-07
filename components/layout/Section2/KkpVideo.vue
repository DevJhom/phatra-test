<script>
export default {
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
  <div>
    <!-- Headings -->
    <div class="kkp-box">
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

    <!-- Youtube and Side Texts -->
    <div class="d-flex">
      <iframe src="https://www.youtube.com/embed/gFLaIDEbJHc" title="KKP Focus">
      </iframe>
      <div class="side-texts">
        <div class="long-line"></div>
        <span class="kkp-focus">{{ active }}</span>
        <span class="kkp-focus-text">
          ฝนนักสู้ พบเรื่องราวจริง เจ็บจริง ประสบความสำเร็จจริง
          ที่จะเป็นแรงกระตุ้นให้ SME นักสู้รุ่นต่อไป ได้ก้าวไปถึงฝัน
        </span>
        <div class="long-line"></div>
      </div>
    </div>
  </div>
</template>

<style scoped>

.kkp-box {
  display: flex;
  margin-bottom: 1.5rem;
}

.clip-heading {
  font-family: Kanit;
  font-size: 1.5rem;
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

.side-texts {
  display: flex;
  flex-direction: column;
  margin: auto 2rem;
}

.long-line {
  width: 266px;
  height: 2px;
  margin: 2rem 0;
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
  font-family: Kanit;
  font-size: 2.625rem;
  font-weight: 500;
  line-height: normal;
  letter-spacing: normal;
  color: #594f74;
}

.kkp-focus-text {
  width: 276px;
  font-family: Kanit;
  font-size: 1.25rem;
  font-weight: normal;
  line-height: 1.4;
  letter-spacing: normal;
  color: #84848f;
}

@media (max-width: 912px) {
  .kkp-box {
    margin-bottom: 1rem;
  }

  .clip-heading {
    font-size: 1rem;
  }

  iframe {
    height: 300px;
  }

  .long-line {
    margin: 1rem 0;
  }

  .kkp-focus {
    font-size: 1.5rem;
  }
  .kkp-focus-text {
    font-size: 0.8rem;
  }
}

@media (max-width: 480px) {
  .kkp-box {
    margin-bottom: 0.5rem;
  }
  .clip-heading {
    font-size: 0.5rem;
  }

  .v-line {
    height: 0.5rem;
    margin: 0 5px;
  }

  iframe {
    height: 150px;
    margin: 0;
  }

  .side-texts {
    margin: auto 0.5rem;
  }

  .long-line {
    width: 100px;
    height: 1px;
  }

  .kkp-focus {
    font-size: 10px;
  }

  .kkp-focus-text {
    width: 100px;
    font-size: 7px;
  }
}
</style>
