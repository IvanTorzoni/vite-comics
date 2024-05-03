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
}

</script>

<template>
    <section class="images">
        <div class="container">
            <div class="options" v-for="icon in icons" :class="{pay : isSvg}">
                <img :src="getImagePath(icon.image)" alt="Digital Comic">
                <span>{{ icon.text }}</span>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>

    @use "../style/partials/mixin" as *;
    @use "../style/partials/variables" as *;

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

    .options{
      &.pay {
          img {
            width: 40%;
            height: 50px;
          }
      }

        display: flex;
        align-items: center;
        height: 50px
    }

    .container {
        @include container(space-between, 80%, 0);
        align-items: center;
    }
}

</style>