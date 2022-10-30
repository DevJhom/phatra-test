<template>
  <div
    class="rectangle"
    :class="active ? 'active' : 'inactive'"
    @click="$emit('clickHandler', text)"
  >
    {{ text }}
  </div>
</template>

<script>
export default {
  name: "Rectangle",
  props: {
    text: String,
    active: Boolean,
  },
};
</script>

<style scoped>
.rectangle {
  display: flex;
  align-items: center;
  width: 16rem;
  height: 5.375rem;
  padding-left: 2rem;
  font-family: "Kanit";
  font-size: 1.25rem;
  font-weight: 500;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.5;
  letter-spacing: normal;
  color: #594f74;
}

.rectangle:hover,
.active {
  color: #fff;
  background-image: linear-gradient(to left, #655a9f, #8b8bc1);
}

.inactive {
  color: #594f74;
  border-bottom: 10px solid #655a9f;
  border-radius: 2px 2px 0 0;
  background-image: linear-gradient(
    to right,
    #eeedf2 3%,
    #ebeaef 34%,
    #e5e5e8 94%
  );
}

@media (max-width: 912px) {
  .rectangle {
    height: 1.5rem;
    font-size: 0.4rem;
    padding-left: 0.5rem;
  }

  .inactive {
    border-bottom: 2px solid #655a9f;
  }
}
</style>
