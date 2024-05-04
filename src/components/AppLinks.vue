<script>
export default {

}

</script>

<template>
    <section class="link">
        <div class="container">
            <div class="links">
                <ul>
                    <li class="title"><h2>DC Comics</h2></li>
                    <li><a href="">Characters</a></li>
                    <li><a href="">Comic</a></li>
                    <li><a href="">Movies</a></li>
                    <li><a href="">TV</a></li>
                    <li><a href="">Games</a></li>
                    <li><a href="">Vidos</a></li>
                    <li><a href="">News</a></li>
                </ul>
                <ul>
                    <li class="title"><h2>Shop</h2></li>
                    <li><a href="">Shop DC</a></li>
                    <li><a href="">Shop DC Collectibles</a></li>
                </ul>
                <ul>
                    <li class="title"><h2>DC</h2></li>
                    <li><a href="">Terms Of Use</a></li>
                    <li><a href="">Privacy policy (New)</a></li>
                    <li><a href="">Add Choices</a></li>
                    <li><a href="">Advertising</a></li>
                    <li><a href="">Jobs</a></li>
                    <li><a href="">Subscriptions</a></li>
                    <li><a href="">Talent Workshops</a></li>
                    <li><a href="">CPSC Certificates</a></li>
                    <li><a href="">Ratings</a></li>
                    <li><a href="">Shop Help</a></li>
                    <li><a href="">Contact US</a></li>
                </ul>
                <ul>
                    <li class="title"><h2>Sites</h2></li>
                    <li><a href="">DC</a></li>
                    <li><a href="">MAD Magazine</a></li>
                    <li><a href="">DC Kids</a></li>
                    <li><a href="">DC Univers</a></li>
                    <li><a href="">DC Power Visa</a></li>
                </ul>
            </div>
            <div class="logo">
                <img src="../assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>

    @use "../style/partials/mixin" as *;
    @use "../style/partials/variables" as *;

.link {
    display: flex;
    height: 500px;
    background-image: url("../assets/img/footer-bg.jpg");
    background-size: cover;
    background-position: center;

    .container {
        @include container(space-around, 80%, 0);

        .links {
            display: flex;
            justify-content: space-around;
            padding-top: 50px;
            width: 50%;
            
            ul {
                list-style-type: none;
                
                
                .title {
                    color: $text-color-links-title;
                    padding-bottom: 20px;
                }

                li {
                    padding-bottom: 10px;
                    
                    a {
                        text-decoration: none;
                        color: $text-color-links;
                    }
                }
            }
        }

        .logo {
            display: flex;
            justify-content: center;
            width: 50%;

            img {
                width: 500px;
            }
        }
    }
}
</style>