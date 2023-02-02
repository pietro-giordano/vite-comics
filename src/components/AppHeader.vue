<script>

export default {
      name: 'AppHeader',
}

</script>

<template>

      <header>
            <div class="container">
                  <div class="logo">
                        <img src="../assets/img/dc-logo.png" alt="dc-logo">
                  </div>

                  <ul>
                        <li>
                              <a href="">
                                    characters
                              </a>
                        </li>
                        <li class="active">
                              <a href="">
                                    comics
                              </a>
                        </li>
                        <li>
                              <a href="">
                                    movies
                              </a>
                        </li>
                        <li>
                              <a href="">
                                    tv
                              </a>
                        </li>
                        <li>
                              <a href="">
                                    games
                              </a>
                        </li>
                        <li>
                              <a href="">
                                    collectibles
                              </a>
                        </li>
                        <li>
                              <a href="">
                                    videos
                              </a>
                        </li>
                        <li>
                              <a href="">
                                    fans
                              </a>
                        </li>
                        <li>
                              <a href="">
                                    news
                              </a>
                        </li>
                        <li>
                              <a href="">
                                    shop
                              </a>
                        </li>
                  </ul>
            </div>
      </header>

</template>

<style lang="scss" scoped>
.container {
      display: flex;
      justify-content: space-between;
      align-items: center;
      height: 100px;

      .logo img {
            width: 80%;
      }

      ul {
            list-style: none;
            text-transform: uppercase;
            display: flex;
            align-items: center;
            font-size: 0.7rem;
            font-weight: bold;

            li {
                  margin: 15px;

                  &.active {
                        color: #0282f9;
                        border-bottom: 4px inset #0282f9;
                  }

                  a {
                        text-decoration: none;
                        color: black;

                  }

            }
      }
}
</style>