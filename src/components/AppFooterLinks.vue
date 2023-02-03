<script>

export default {
      name: 'AppFooterLinks',
      data() {
            return {

            }
      }
}
</script>

<template>

      <section>

            <div class="container">
                  <div class="links">
                        <div>
                              <h3>dc comics</h3>
                              <ul>
                                    <li>
                                          <a href="">Characters</a>
                                    </li>
                                    <li>
                                          <a href="">Comics</a>
                                    </li>
                                    <li>
                                          <a href="">Movies</a>
                                    </li>
                                    <li>
                                          <a href="">TV</a>
                                    </li>
                                    <li>
                                          <a href="">Games</a>
                                    </li>
                                    <li>
                                          <a href="">Videos</a>
                                    </li>
                                    <li>
                                          <a href="">News</a>
                                    </li>
                              </ul>

                              <h3>shop</h3>
                              <ul>
                                    <li>
                                          <a href="">Shop DC</a>
                                    </li>
                                    <li>
                                          <a href="">Shop DC Collectibles</a>
                                    </li>
                              </ul>
                        </div>

                        <div>
                              <h3>dc</h3>
                              <ul>
                                    <li>
                                          <a href="">Terms Of Use</a>
                                    </li>
                                    <li>
                                          <a href="">Privacy Policy (new)</a>
                                    </li>
                                    <li>
                                          <a href="">Ad Choices</a>
                                    </li>
                                    <li>
                                          <a href="">Advertising</a>
                                    </li>
                                    <li>
                                          <a href="">Jobs</a>
                                    </li>
                                    <li>
                                          <a href="">Subscriptions</a>
                                    </li>
                                    <li>
                                          <a href="">Talent Workshops</a>
                                    </li>
                                    <li>
                                          <a href="">CPSC Certificates</a>
                                    </li>
                                    <li>
                                          <a href="">Ratings</a>
                                    </li>
                                    <li>
                                          <a href="">Shop Help</a>
                                    </li>
                                    <li>
                                          <a href="">Contact Us</a>
                                    </li>
                              </ul>
                        </div>

                        <div>
                              <h3>sites</h3>
                              <ul>
                                    <li>
                                          <a href="">DC</a>
                                    </li>
                                    <li>
                                          <a href="">MAD Magazine</a>
                                    </li>
                                    <li>
                                          <a href="">DC Kids</a>
                                    </li>
                                    <li>
                                          <a href="">DC Universe</a>
                                    </li>
                                    <li>
                                          <a href="">DC Power Visa</a>
                                    </li>
                              </ul>
                        </div>
                  </div>

                  <!-- <img src="../assets/img/dc-logo-bg.png" alt=""> -->
            </div>

      </section>

</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;

section {
      background-image: url('../assets/img/footer-bg.jpg');
      padding-top: 30px;
      padding-bottom: 30px;

      .container {
            @include container;
            @include flex(row, space-between);

            .links {
                  display: flex;

                  >div {
                        margin-right: 20px;

                        h3 {
                              color: white;
                              text-transform: uppercase;
                              margin-bottom: 5px;
                        }

                        ul {
                              list-style: none;
                              margin-bottom: 20px;

                              a {
                                    color: #929387;
                                    text-decoration: none;
                                    font-size: 0.6rem;
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