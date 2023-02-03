<script>

export default {
      name: 'AppFooterBuy',
      data() {
            return {
                  links: [
                        {
                              label: 'digital comics',
                              src: 'buy-comics-digital-comics.png',
                              url: '#'
                        }, {
                              label: 'digital comics',
                              src: 'buy-comics-digital-comics.png',
                              url: '#'
                        }, {
                              label: 'digital comics',
                              src: 'buy-comics-digital-comics.png',
                              url: '#'
                        }, {
                              label: 'digital comics',
                              src: 'buy-comics-digital-comics.png',
                              url: '#'
                        }, {
                              label: 'digital comics',
                              src: 'buy-comics-digital-comics.png',
                              url: '#'
                        },
                  ]
            }
      },
      methods: {
            getImagePath: function (imgPath) {
                  return new URL(imgPath, import.meta.url).href;
            }
      }
}
</script>

<template>

      <section>

            <div class="container">
                  <div v-for="link in links">
                        <img :src="getImagePath(`../assets/img/${link.src}`)" :alt="link.label">
                        <a :href="link.url">{{ link.label }}</a>
                  </div>
            </div>

      </section>

</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;

section {
      background-color: $main-blue;

      .container {
            @include container;
            @include flex(row, space-around);

            div {
                  @include flex(row, center, center);
                  height: 140px;
                  background-color: $main-blue;
                  width: calc((1000px / 5) - 20px);

                  a {
                        text-decoration: none;
                        text-transform: uppercase;
                        color: white;
                        font-size: 0.8rem;
                        padding: 5px;
                  }

                  img {
                        display: inline-block;
                        max-width: 40px;
                        max-height: 40px;
                  }
            }
      }
}
</style>