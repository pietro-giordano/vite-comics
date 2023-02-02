<script>

export default {
      name: 'AppFooterFooter',
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
                        <a href="">
                              <img src="../assets/img/footer-facebook.png" alt="">
                        </a>
                        <a href="">
                              <img src="../assets/img/footer-twitter.png" alt="">
                        </a>
                        <a href="">
                              <img src="../assets/img/footer-youtube.png" alt="">
                        </a>
                        <a href="">
                              <img src="../assets/img/footer-pinterest.png" alt="">
                        </a>
                        <a href="">
                              <img src="../assets/img/footer-periscope.png" alt="">
                        </a>
                  </div>
            </div>

      </section>

</template>

<style lang="scss" scoped>
section {
      background-color: #303030;

      .container {
            padding-top: 20px;
            padding-bottom: 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;

            button {
                  text-transform: uppercase;
                  color: white;
                  padding: 10px;
                  background-color: #303030;
                  border: 2px solid #0282f9;
            }

            div {
                  display: flex;
                  align-items: center;

                  h3 {
                        text-transform: uppercase;
                        color: #0282f9;
                  }

                  img {}

                  >* {
                        margin: 10px;
                  }
            }
      }
}
</style>