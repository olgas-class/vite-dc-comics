<script>
export default {
    name: "ComicCard",
    props: {
        // imgSrc: String,
        // title: String
        comicObj: Object
    }
}
</script>

<template>
    <div class="card">
        <img class="card-img" :src="comicObj.thumb" alt="">
        <h3 class="card-serie">{{ comicObj.series }}</h3>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.card {
    width: calc(100% / 6 - 10px);
    margin-bottom: 5px;

    &-serie {
        color: $dark_section_text_color;
    }
}
</style>