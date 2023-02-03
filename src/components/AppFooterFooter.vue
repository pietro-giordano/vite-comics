<script>

export default {
      name: 'AppFooterFooter',
      data() {
            return {
                  social: [
                        {
                              label: 'facebook',
                              url: '#',
                              src: "footer-facebook.png"
                        }, {
                              label: 'twitter',
                              url: '#',
                              src: "footer-twitter.png"
                        }, {
                              label: 'youtube',
                              url: '#',
                              src: "footer-youtube.png"
                        }, {
                              label: 'pinterest',
                              url: '#',
                              src: "footer-pinterest.png"
                        }, {
                              label: 'periscope',
                              url: '#',
                              src: "footer-periscope.png"
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
                  <button>
                        sign-up now!
                  </button>

                  <div>
                        <h3>Follow Us</h3>
                        <a v-for="a in social" :href="a.label">
                              <img :src="getImagePath(`../assets/img/${a.src}`)" :alt="a.label">
                        </a>
                  </div>
            </div>

      </section>

</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;

section {
      background-color: $footer-gray;

      .container {
            @include container;
            @include flex(row, space-between, center);
            padding: 20px 0;

            button {
                  text-transform: uppercase;
                  color: white;
                  padding: 10px;
                  background-color: $footer-gray;
                  border: 2px solid $main-blue;
            }

            div {
                  @include flex(row, flex-start, center);

                  h3 {
                        text-transform: uppercase;
                        color: $main-blue;
                  }

                  img {}

                  >* {
                        margin: 10px;
                  }
            }
      }
}
</style>