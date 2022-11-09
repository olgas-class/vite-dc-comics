<script>
export default {
    name: "ComicsList"
}
</script>

<template>
    <section class="main-bg">
        <h2>Lista dei comics</h2>
    </section>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.main-bg {
    padding: 2rem 0;
    background-color: $dark_section_bg_color;

    h2 {
        text-align: center;
        color: $dark_section_text_color;
    }
}
</style>