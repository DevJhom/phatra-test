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
  width: 15vw;
  height: 4.5vw;
  padding-left: 1.5rem;
  font-family: "Kanit";
  font-size: 1.1rem;
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

@media (max-width: 1080px) {
  .rectangle {
    height: 3rem;
    font-size: 0.8rem;
    padding-left: 0.5rem;
  }

  .inactive {
    border-bottom: 5px solid #655a9f;
  }
}

@media (max-width: 480px) {
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
