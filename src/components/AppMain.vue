<script>
export default {
  data() {
    return {
      icons: [
        {
          image: "buy-comics-digital-comics.png",
          text: "DIGITAL COMICS",
          isSvg: false,
        },
        {
          image: "buy-comics-merchandise.png",
          text: "DC MERCHANDISE",
          isSvg: false,
        },
        {
          image: "buy-comics-subscriptions.png",
          text: "SUBSCRIPTION",
          isSvg: false,
        },
        {
          image: "buy-comics-shop-locator.png",
          text: "COMICS SHOP LOCATOR",
          isSvg: false,
        },
        {
          image: "buy-dc-power-visa.svg",
          text: "DC POWER VISA",
          isSvg: true,
        },
      ],
    };
  },
  methods: {
    getImagePath(curImage) {
      return new URL(`../assets/img/${curImage}`, import.meta.url).href;
    },
  },
};

</script>

<template>
    <section class="content">
        <div class="container">
            <h2> --> Content goes here <-- </h2>
        </div>
    </section>
    <section class="images">
        <div class="container">
            <div class="options" v-for="icon in icons">
                <img :src="getImagePath(icon.image)" :class="{pay : isSvg = true}" alt="Digital Comic">
                <span>{{ icon.text }}</span>
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
        max-width: 100%;
        padding-right: 30px;
    }

    .pay{
        width: 50%
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