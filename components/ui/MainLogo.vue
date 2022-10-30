<template>
  <img
    src="@/assets/logo-copy/logo-copy.png"
    srcset="
      @/assets/logo-copy/logo-copy@2x.png 2x,
      /@assets/logo-copy/logo-copy@3x.png 3x
    "
    alt="Logo"
    class="logo-copy"
  />
</template>

<style scoped>
img.logo-copy {
  width: 12.5rem;
  height: 3.4rem;
  object-fit: contain;
}

@media (max-width: 912px) {
   img.logo-copy {
      width: 6rem;
      height: 1.7rem;
   }
}

</style>
