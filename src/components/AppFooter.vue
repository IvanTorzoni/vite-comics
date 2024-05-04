<script>
export default {

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
                    <img src="../assets/img/footer-facebook.png" alt="">
                    <img src="../assets/img/footer-twitter.png" alt="">
                    <img src="../assets/img/footer-youtube.png" alt="">
                    <img src="../assets/img/footer-pinterest.png" alt="">
                    <img src="../assets/img/footer-periscope.png" alt="">
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
    background-color: #303030;

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
                    border: 2px solid #0085ff;
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
                    color: #037ef1;
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