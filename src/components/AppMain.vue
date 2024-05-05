<script>
import { comicsArray } from "../assets/data/comic.js";
import ComicDisplayer from "./ComicDisplayer.vue";


export default {
    components: {
        ComicDisplayer,
    },
    data() {
        return {
            comic: comicsArray,
        };
    },
};

</script>

<template>
    <section class="content">
        <div class="container">
            <div class="row">
                <div class="col" v-for="comicDisplay in comic">
                    <ComicDisplayer 
                    :comicImage="comicDisplay.thumb" 
                    :comicSeries="comicDisplay.series" 
                    />
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

.content {
    display: flex;
    align-items: center;
    height: 800px;
    width: 100%;
    margin-top: 30px;
    background-color: $bg-color-content;
    color: $color-content;

    .container {
        @include container(space-between, 80%, 0);


        .row {
            display: flex;
            flex-direction: row;
            align-items: stretch;
            flex-wrap: wrap;
        }
        .col {
            width: 15%;
            margin-bottom: 1rem;
            color: white;
        }

        }
    }</style>