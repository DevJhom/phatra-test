<template>
  <div class="container d-flex justify-content-between">
    <img
      src="@/assets/footer/logo-footer-1/logo-footer-1.jpg"
      srcset="
        @/assets/footer/logo-footer-1/logo-footer-1@2x.jpg 2x,
        @/assets/footer/logo-footer-1/logo-footer-1@3x.jpg 3x
      "
      class="logo_footer1"
    />
    <img
      src="@/assets/footer/logo-footer-2/logo-footer-2.jpg"
      srcset="
        @/assets/footer/logo-footer-2/logo-footer-2@2x.jpg 2x,
        @/assets/footer/logo-footer-2/logo-footer-2@3x.jpg 3x
      "
      class="logo_footer2"
    />
    <img
      src="@/assets/footer/logo-footer-3/logo-footer-3.jpg"
      srcset="
        @/assets/footer/logo-footer-3/logo-footer-3@2x.jpg 2x,
        @/assets/footer/logo-footer-3/logo-footer-3@3x.jpg 3x
      "
      class="logo_footer3"
    />
    <img
      src="@/assets/footer/logo-footer-4/logo-footer-4.jpg"
      srcset="
        @/assets/footer/logo-footer-4/logo-footer-4@2x.jpg 2x,
        @/assets/footer/logo-footer-4/logo-footer-4@3x.jpg 3x
      "
      class="logo_footer1"
    />
  </div>
</template>

<style scoped>
img.logo_footer1 {
  width: clamp(5vw, 270px, 20vw);
  height: auto;
  object-fit: contain;
}

img.logo_footer2 {
  width: clamp(5vw, 170px, 20vw);
  height: auto;
  object-fit: contain;
}

img.logo_footer3 {
  width: clamp(5vw, 230px, 20vw);
  height: auto;
  object-fit: contain;
}

img.logo_footer4 {
  width: clamp(5vw, 170px, 20vw);
  height: auto;
  object-fit: contain;
}
</style>
