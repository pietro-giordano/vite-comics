<script>

export default {
      name: 'AppHeader',
      data() {
            return {
                  links: [
                        {
                              label: 'characters',
                              url: '#',
                              active: false,
                        }, {
                              label: 'comics',
                              url: '#',
                              active: true,
                        }, {
                              label: 'movies',
                              url: '#',
                              active: false,
                        }, {
                              label: 'tv',
                              url: '#',
                              active: false,
                        }, {
                              label: 'games',
                              url: '#',
                              active: false,
                        }, {
                              label: 'collectibles',
                              url: '#',
                              active: false,
                        }, {
                              label: 'videos',
                              url: '#',
                              active: false,
                        }, {
                              label: 'fans',
                              url: '#',
                              active: false,
                        }, {
                              label: 'news',
                              url: '#',
                              active: false,
                        }, {
                              label: 'shop',
                              url: '#',
                              active: false,
                        },
                  ]
            }
      }
}

</script>

<template>

      <header>
            <div class="container">
                  <div class="logo">
                        <img src="../assets/img/dc-logo.png" alt="dc-logo">
                  </div>

                  <ul>
                        <li v-for="link in links">
                              <a :href="link.url" :class="{ active: link.active }">
                                    {{ link.label }}
                              </a>
                        </li>
                  </ul>
            </div>
      </header>

</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;

.container {
      @include container;
      @include flex(row, space-between, center);
      height: 100px;

      .logo img {
            width: 80%;
      }

      ul {
            @include flex(row, flex-start, center);
            list-style: none;
            text-transform: uppercase;
            font-size: 0.7rem;
            font-weight: bold;
            height: 100%;

            li {
                  @include flex(row, center, center);
                  margin: 0px 15px;
                  height: 100%;
                  position: relative;

                  a {
                        text-decoration: none;
                        color: black;

                        &.active {
                              color: $main-blue;

                              &::after {
                                    bottom: 0;
                                    content: '';
                                    display: block;
                                    background-color: $main-blue;
                                    height: 5px;
                                    width: 100%;
                                    position: absolute;
                              }
                        }

                  }
            }

      }
}
</style>