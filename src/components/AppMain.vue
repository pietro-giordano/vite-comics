<script>
import DcComics from '../assets/dc-comics.json';

export default {
      name: 'AppMain',
      data() {
            return {
                  comics: DcComics,
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

      <main>
            <div class="jumbotron">
                  <img src="../assets/img/jumbotron.jpg" alt="teen titans">
            </div>

            <div class="container">
                  <div v-for="card in comics" class="card">
                        <img :src="card.thumb" :alt="card.series">
                        <p>{{ card.series }}</p>
                  </div>
            </div>
      </main>

</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;

main {
      background-color: $main-gray;

      .jumbotron {
            height: 300px;

            img {
                  height: 100%;
                  width: 100%;
                  object-fit: cover;
                  object-position: top;
            }
      }

      .container {
            @include container;
            @include flex(row, space-between, center);
            flex-wrap: wrap;
            color: white;
            font-size: 1.3rem;
            margin-top: 50px;

            .card {
                  width: calc((100% / 6) - 20px);
                  height: 200px;
                  margin-bottom: 20px;

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
            }
      }
}
</style>