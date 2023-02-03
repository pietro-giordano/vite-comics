<script>

export default {
      name: 'AppFooterLinks',
      data() {
            return {
                  sections: [
                        {
                              title: 'dc comics',
                              links: [
                                    {
                                          label: 'Characters',
                                          url: '#'
                                    }, {
                                          label: 'Comics',
                                          url: '#'
                                    }, {
                                          label: 'Movies',
                                          url: '#'
                                    }, {
                                          label: 'TV',
                                          url: '#'
                                    }, {
                                          label: 'Games',
                                          url: '#'
                                    }, {
                                          label: 'Videos',
                                          url: '#'
                                    }, {
                                          label: 'News',
                                          url: '#'
                                    },
                              ]
                        }, {
                              title: 'shop',
                              links: [
                                    {
                                          label: 'Shop DC',
                                          url: '#'
                                    }, {
                                          label: 'Shop DC Collectibles',
                                          url: '#'
                                    },
                              ]
                        }, {
                              title: 'dc',
                              links: [
                                    {
                                          label: 'Terms Of Use',
                                          url: '#'
                                    }, {
                                          label: 'Privacy Policy (New)',
                                          url: '#'
                                    }, {
                                          label: 'Add Choices',
                                          url: '#'
                                    }, {
                                          label: 'Advertising',
                                          url: '#'
                                    }, {
                                          label: 'Jobs',
                                          url: '#'
                                    }, {
                                          label: 'Subscriptions',
                                          url: '#'
                                    }, {
                                          label: 'Talent Workshops',
                                          url: '#'
                                    }, {
                                          label: 'CPSC Certificates',
                                          url: '#'
                                    }, {
                                          label: 'Ratings',
                                          url: '#'
                                    }, {
                                          label: 'Shop Help',
                                          url: '#'
                                    }, {
                                          label: 'Contact Us',
                                          url: '#'
                                    },
                              ]
                        }, {
                              title: 'sites',
                              links: [
                                    {
                                          label: 'DC',
                                          url: '#'
                                    }, {
                                          label: 'MAD Magazine',
                                          url: '#'
                                    }, {
                                          label: 'DC Kids',
                                          url: '#'
                                    }, {
                                          label: 'DC Universe',
                                          url: '#'
                                    }, {
                                          label: 'DC Power Visa',
                                          url: '#'
                                    },
                              ]
                        },
                  ]
            }
      }
}
</script>

<template>

      <section>

            <div class="container">
                  <div class="links">
                        <div v-for="section in sections">
                              <h3>{{ section.title }}</h3>
                              <ul>
                                    <li v-for="link in section.links">
                                          <a :href="link.url">{{ link.label }}</a>
                                    </li>
                              </ul>
                        </div>
                  </div>
            </div>

      </section>

</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;

section {
      background-image: url('../assets/img/footer-bg.jpg');
      height: 330px;

      .container {
            @include container;
            height: 100%;

            .links {
                  @include flex(column);
                  flex-wrap: wrap;
                  align-content: flex-start;
                  padding: 30px 0px;
                  height: 100%;
                  background-image: url('../assets/img/dc-logo-bg.png');
                  background-size: 500px;
                  background-position: right;
                  background-repeat: no-repeat;

                  >div {
                        margin-right: 30px;

                        h3 {
                              color: white;
                              text-transform: uppercase;
                              margin-bottom: 5px;
                        }

                        ul {
                              list-style: none;
                              margin-bottom: 20px;

                              a {
                                    color: $footer-links;
                                    text-decoration: none;
                                    font-size: 0.6rem;

                                    &:hover {
                                          color: $main-blue;
                                    }
                              }
                        }
                  }
            }

            img {
                  display: inline-block;

            }
      }
}
</style>