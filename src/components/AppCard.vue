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
img {
      width: 100%;
      height: 150px;
      object-fit: cover;
      object-position: top;
      padding-bottom: 10px;
}

p {
      text-transform: uppercase;
      font-size: 0.8rem;
}
</style>