<script>
export default {
    data() {
    return {
      icons: [
        {
          image: "footer-facebook.png",
        },
        {
          image: "footer-twitter.png",
        },
        {
          image: "footer-youtube.png",
        },
        {
          image: "footer-pinterest.png",
        },
        {
          image: "footer-periscope.png",
        },
      ],
    };
  },
  methods: {
    getImagePath(curImage) {
      return new URL(`../assets/img/${curImage}`, import.meta.url).href;
    },
  },
}

</script>

<template>
    <section class="footer">
        <div class="container">
            <div class="content">
                <div class="sign-up">
                    <span><a href="">SIGN-UP NOW!</a></span>
                </div>
                <div class="icons">
                    <span>Follow Us</span>
                    <a href="" v-for="social in icons"><img :src="getImagePath(social.image)" alt=""></a>
                </div>
            </div>


        </div>
    </section>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;


.footer {
    height: 100px;
    background-color: $bg-color-footer;

    .container {
        @include container(space-between, 80%, 0);


        .content {
            display: flex;
            height: 100px;
            width: 100%;
            align-items: center;
            justify-content: space-evenly;
            
            .sign-up{
                width: 50%;

                a {
                    padding: 10px;
                    border: 2px solid $border-color-sign-up;
                    text-decoration: none;
                    color: white;
                }       
            }


            .icons {
                display: flex;
                justify-content: end;
                align-items: center;
                width: 50%;

                span{
                    color: $color-follow-us;
                    font-size: 30px;
                    font-family: Arial, Helvetica, sans-serif;
                }

                img {
                    padding-left: 30px;
                }
            }
        }
    }
}
</style>