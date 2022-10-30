<script>
export default {
    name: "PlaceHolder",
    props: {
        text: String
    }
}
</script>

<template>
  <div class="container">
    <div class="d-flex articles">
      {{text}}
    </div>
  </div>
</template>

<style scoped>
.articles {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 50vh;
  margin: 10px;
  color: #fff;
  border-radius: 2px;
  background-color: gray;
}
</style>
