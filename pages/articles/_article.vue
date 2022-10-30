<template>
  <place-holder :text="$route.params.article">
  </place-holder>
</template>

<script>
import PlaceHolder from '../../components/ui/PlaceHolder.vue'

export default {
  components: {
    PlaceHolder
  }
}
</script>
