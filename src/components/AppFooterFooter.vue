<script>

export default {
      name: 'AppFooterFooter',
}
</script>

<template>

      <section>



      </section>

</template>

<style lang="scss" scoped>
section {
      background-color: #0282f9;

      .container {
            display: flex;
            justify-content: space-around;

            div {
                  height: 150px;
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