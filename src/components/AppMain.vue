<script>
import DcComics from '../assets/dc-comics.json';
import AppCard from './AppCard.vue';

export default {
      name: 'AppMain',
      components: {
            AppCard
      },
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
            </div>

            <div class="container">
                  <div class="current-button">
                        <button>
                              current series
                        </button>
                  </div>

                  <div class="card-container">
                        <AppCard v-for="card in comics" class="card" :series="card.series" :thumb="card.thumb" />
                  </div>

                  <div class="load-button">
                        <button>
                              load more
                        </button>
                  </div>
            </div>
      </main>

</template>

<style lang="scss">
@use '../styles/partials/mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;

main {
      background-color: $main-gray;

      .jumbotron {
            height: 300px;
            background-image: url('../assets/img/jumbotron.jpg');
            background-size: cover;
      }

      .container {
            @include container;
            color: white;
            font-size: 1.3rem;
            padding-top: 50px;
            position: relative;

            button {
                  background-color: $main-blue;
                  color: white;
                  font-weight: bold;
                  text-transform: uppercase;
                  border: none;
                  cursor: pointer;
            }

            .current-button {
                  position: absolute;
                  top: 0;
                  left: 0;
                  transform: translateY(-50%);

                  button {
                        padding: 8px 15px;
                        font-size: 1.3rem
                  }
            }

            .load-button {
                  @include flex(row, center, center);
                  padding-bottom: 15px;

                  button {
                        padding: 8px 30px;
                        font-size: 0.8rem;
                  }
            }

            .card-container {
                  @include flex(row, space-around, center);
                  flex-wrap: wrap;

                  .card {
                        width: calc((100% / 6) - 20px);
                        height: 200px;
                        margin-bottom: 20px;
                        cursor: pointer;

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


}
</style>