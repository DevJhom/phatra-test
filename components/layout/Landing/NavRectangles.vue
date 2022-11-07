<script>
import Rectangle from "../../ui/Rectangle.vue";

export default {
  name: "NavRectangles",
  components: {
    Rectangle,
  },
  data() {
    return {
      active: "About Us",
    };
  },
  methods: {
    activePrev() {
      if (this.active === "About Us") {
        this.active = "Awards";
      } else if (this.active === "Awards") {
        this.active = "Our Businesses";
      } else if (this.active === "Our Businesses") {
        this.active = "News & Activities";
        console.log(this.active);
      } else if (this.active === "News & Activities") {
        this.active = "About Us";
      }
    },
    activeNext() {
      if (this.active === "About Us") {
        this.active = "News & Activities";
      } else if (this.active === "Awards") {
        this.active = "About Us";
      } else if (this.active === "Our Businesses") {
        this.active = "Awards";
        console.log(this.active);
      } else if (this.active === "News & Activities") {
        this.active = "Our Businesses";
      }
    },
    changeActiveStatus(text) {
      this.active = text;
      console.log(this.active);
    },
  },
};
</script>

<template>
  <div class="container component-wrapper">
    <div class="d-flex justify-content-center gap-2">
      <img
        @click="activeNext"
        src="@/assets/icons/left-arrow/bt-back.png"
        alt="left-arrow"
        class="icons"
      />
      <Rectangle
        text="About Us"
        :active="active === 'About Us' ? true : false"
        @clickHandler="changeActiveStatus"
      />
      <Rectangle
        text="Awards"
        :active="active === 'Awards' ? true : false"
        @clickHandler="changeActiveStatus"
      />
      <Rectangle
        text="Our Businesses"
        :active="active === 'Our Businesses' ? true : false"
        @clickHandler="changeActiveStatus"
      />
      <Rectangle
        text="News & Activities"
        :active="active === 'News & Activities' ? true : false"
        @clickHandler="changeActiveStatus"
      />
      <img
        @click="activePrev"
        src="@/assets/icons/right-arrow/bt-next.png"
        alt="right-arrow"
        class="icons"
      />
    </div>
  </div>
</template>

<style scoped>
.component-wrapper {
  position: relative;
  margin-top: -25px;
  width: 100vw;
}

img.icons {
  margin: auto 25px;
  width: 25px;
  height: 33px;
}

img.icons:hover {
  cursor: pointer;
}

@media (max-width: 912px) {
  .component-wrapper {
    margin-top: -8px;
  }

  img.icons {
    margin: auto 10px;
    width: 10px;
    height: 10px;
  }
}
</style>
