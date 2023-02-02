<script>

export default {
      name: 'AppFooterBuy',
}
</script>

<template>

      <section>

            <div class="container">
                  <div>
                        <img src="../assets/img/buy-comics-digital-comics.png" alt="">
                        <a href="">digital comics</a>
                  </div>
                  <div>
                        <img src="../assets/img/buy-comics-merchandise.png" alt="">
                        <a href="">dc merchandise</a>
                  </div>
                  <div>
                        <img src="../assets/img/buy-comics-subscriptions.png" alt="">
                        <a href="">subscription</a>
                  </div>
                  <div>
                        <img src="../assets/img/buy-comics-shop-locator.png" alt="">
                        <a href="">comic shop locator</a>
                  </div>
                  <div>
                        <img src="../assets/img/buy-dc-power-visa.svg" alt="">
                        <a href="">dc power visa</a>
                  </div>
            </div>

      </section>

</template>

<style lang="scss" scoped>
section {
      background-color: #0282f9;

      .container {
            display: flex;
            justify-content: space-around;

            div {
                  height: 140px;
                  background-color: #0282f9;
                  display: flex;
                  align-items: center;
                  justify-content: center;
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