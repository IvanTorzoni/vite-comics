<script>
    export default {
        data() {
            return {
                // Inserimento del menù di navigazione dinamico
                menu: [
                    {
                        title: "CHARACTERS",
                        isActive: false,
                    },
                    {
                        title: "COMICS",
                        isActive: true,
                    },
                    {
                        title: "MOVIES",
                        isActive: false,
                    },
                    {
                        title: "TV",
                        isActive: false,
                    },
                    {
                        title: "GAMES",
                        isActive: false,
                    },
                    {
                        title: "COLLECTABLES",
                        isActive: false,
                    },
                    {
                        title: "VIDEOS",
                        isActive: false,
                    },
                    {
                        title: "FANS",
                        isActive: false,
                    },
                    {
                        title: "NEWS",
                        isActive: false,
                    },
                    {
                        title: "SHOP",
                        isActive: false,
                    },
                ],
            };
        },
    };
</script>

<template>
    <header>
        <div class="container">
            <!-- Logo -->
            <span class="header-logo">
                <img src="../assets/img/dc-logo.png" alt="DC logo">
            </span>
            <!-- Menù dinamico -->
            <ul class="navigation">
                <li v-for="item in menu" :class="{ active : item.isActive }">
                    <a href="" > {{ item.title }} </a>
                </li>
            </ul>
        </div>
    </header>
</template>

<!-- Stile del componente -->
<style scoped lang="scss">
    @use "../style/partials/mixin" as *;
    @use "../style/partials/variables" as *;


    .container {
        @include container(space-between, 80%, 0);

        .header-logo{
            margin-top: 20px
        }

        ul {
            @include flex(row, center, center);
            list-style-type: none;

            li {

                &.active {
                    a {
                        color: $text-colore-active-nav
                        
                    }
                }

                a {
                    color: $text-color-nav;
                    font-size: 16px;
                    padding: 10px 16px;
                    text-decoration: none;
                    display: inline-block;
                }
            }
        }
    }
</style>