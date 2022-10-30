<template>
  <div class="wrapper">
    <span class="set_index">Set Index</span>
    <img
      src="@/assets/set-index/set-index.jpg"
      srcset="
        @/assets/set-index/set-index@2x.jpg 2x,
        @/assets/set-index/set-index@3x.jpg 3x
      "
      class="set_index"
    />
  </div>
</template>

<style scoped>
.wrapper {
  margin: 36px 0 0 0px;
  padding: 10px 32px 21px 43px;
  background-color: #fff;
}

.set_index {
  font-family: Kanit;
  font-size: 1.75rem;
  font-weight: 500;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.43;
  letter-spacing: normal;
  color: #594f74;
}

img.set_index {
  margin: 8px 0 0 6px;
  object-fit: contain;
}

@media (max-width: 912px) {
  .set_index {
    font-size: 1rem;
  }

  img.set_index {
    width: 200px;
    height: auto;
  }
}
</style>
