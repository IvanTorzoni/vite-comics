<script>
export default {

}

</script>

<template>
    <section class="content">
        <div class="container">
            <h2> --> Content goes here <-- </h2>
        </div>
    </section>
    <section class="images">
        <div class="container">
            <div class="options">
                <img src="../assets/img/buy-comics-digital-comics.png" alt="Digital Comic">
                <span>DIGITAL COMICS</span>
            </div>
            <div class="options">
                <img src="../assets/img/buy-comics-merchandise.png" alt="Merch">
                <span>DC MERCHANDISE</span>
            </div>
            <div class="options">
                <img src="../assets/img/buy-comics-subscriptions.png" alt="Subscription">
            <span>SUBSCRIPTION</span>                
            </div>
            <div class="options">
                <img src="../assets/img/buy-comics-shop-locator.png" alt="Closest Store">
            <span>COMIC SHOP LOCATOR</span>                
            </div>
            <div class="options">
                <img class="pay" src="../assets/img/buy-dc-power-visa.svg" alt="Payment methods">
            <span>DC POWER VISA</span>                
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
    @use "../style/partials/mixin" as *;
    @use "../style/partials/variables" as *;

.content{
    display: flex;
    align-items: center;
    width: 100%;
    margin-top: 30px;
    background-color: $bg-color-content;
    color: $color-content;
    height: 200px;

    .container {
        @include container(space-between, 80%, 0);
    }
}

.images {
    display: flex;
    width: 100%;
    background-color: $bg-color-images;
    color: $color-images;
    height: 200px;

    img{
        max-width: 50%;
        padding-right: 30px;
    }

    .pay{
        width: 40%
    }

    .options{
        display: flex;
        align-items: center
    }

    .container {
        @include container(space-between, 80%, 0);
        align-items: center;
    }
}

</style>