<template>
  <modal name="restaurant-info" @before-open="beforeOpen">
    <a :href="url">{{ url }}</a>
  </modal>
</template>
<script>
export default {
  data() {
    return {
      restaurant: null
    }
  },
  computed: {
    url() {
      return this.restaurant ? this.restaurant.urls.pc : ''
    }
  },
  methods: {
    beforeOpen(e) {
      console.log(e)
      this.restaurant = e.params.restaurant
    }
  }
}
</script>
<style lang="scss" scoped>

</style>
