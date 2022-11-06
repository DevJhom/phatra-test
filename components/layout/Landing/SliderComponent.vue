<template>
  <div id="mySlideshow" class="carousel slide" data-ride="carousel" data-interval="false">
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img
          class="d-block w-100"
          src="@/assets/slides/slide.jpg"
          srcset="
            @/assets/slides/slide@2x.jpg 2x,
            @/assets/slides/slide@3x.jpg 3x
          "
          alt="First slide"
        />
      </div>
      <div class="carousel-item">
        <img
          class="d-block w-100"
          src="@/assets/slides/slide.jpg"
          srcset="
            @/assets/slides/slide@2x.jpg 2x,
            @/assets/slides/slide@3x.jpg 3x
          "
          alt="Second slide"
        />
      </div>
      <div class="carousel-item">
        <img
          class="d-block w-100"
          src="@/assets/slides/slide.jpg"
          srcset="
            @/assets/slides/slide@2x.jpg 2x,
            @/assets/slides/slide@3x.jpg 3x
          "
          alt="Third slide"
        />
      </div>
    </div>
    <a
      class="carousel-control-prev"
      href="#mySlideshow"
      role="button"
      data-slide="prev"
    >
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    </a>
    <a
      class="carousel-control-next"
      href="#mySlideshow"
      role="button"
      data-slide="next"
    >
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
    </a>
  </div>
</template>

<style scoped>
@media (max-width: 912px) {
  * {
    background-color: #21201a;
  }

  img {
    padding-top: 50px;
  }
}
</style>
