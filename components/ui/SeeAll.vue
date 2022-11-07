<script>
export default {
  name: "SeeAll",
  props: {
    link: String,
  },
};
</script>

<template>
  <nuxt-link class="d-flex" :to="link + ''">
    <span class="me-2 text">ดูทั้งหมด</span>
    <div class="circle">
      <img
        class="icon"
        src="@/assets/icons/right-arrow/bt-next.png/"
        alt="action-icon"
      />
    </div>
  </nuxt-link>
</template>

<style scoped>
.text {
  margin: 0 4px 4px 0;
  font-family: Tahoma;
  font-size: 1rem;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.5;
  letter-spacing: normal;
  color: #84848f;
}

.text:hover {
  color: #8272ab;
}

.circle {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 28px;
  height: 28px;
  border: 0.5px solid #adacb9;
  border-radius: 50%;
}

.icon {
  width: 10px;
  height: 12px;
}

a {
  text-decoration: none;
}

@media (max-width: 912px) {
  .text {
    font-size: 0.8rem;
  }

  .circle {
    width: 20px;
    height: 20px;
  }

  .icon {
    width: 8px;
    height: 10px;
  }
}

@media (max-width: 425px) {
  .text {
    font-size: 0.5rem;
  }

  .circle {
    width: 14px;
    height: 14px;
  }

  .icon {
    width: 5px;
    height: 6px;
  }
}
</style>
