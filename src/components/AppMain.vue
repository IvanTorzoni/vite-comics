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
</style>