<script>
export default {
      name: 'AppCard',
      props: {
            thumb: String,
            series: String,
      }
}
</script>

<template>
      <div>
            <img :src="thumb" :alt="series">
            <p>{{ series }}</p>
      </div>
</template>

<style lang="scss" scoped>

</style>