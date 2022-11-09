<script>
export default {
    name: "AppIcons",
    data() {
        return {
            icons: [
                {
                    img: 'buy-comics-digital-comics.png',
                    title: "Digital comics"
                },
                {
                    img: 'buy-comics-merchandise.png',
                    title: "Digital comics"
                },
                {
                    img: 'buy-comics-digital-comics.png',
                    title: "Digital comics"
                },
                {
                    img: 'buy-comics-digital-comics.png',
                    title: "Digital comics"
                },
                {
                    img: 'buy-dc-power-visa.svg',
                    title: "DC Power Visa"
                }
            ]
        }
    },
    methods: {
        getImageUrl(url) {
            return new URL(url, import.meta.url).href;
        }
    }
}
</script>

<template>
    <section class="primary-bg icons-section">
        <div class="small-container">
            <ul class="flex-row justify-between">
                <li class="flex-row" v-for="(icon, index) in icons" :key="index">
                    <img :src="getImageUrl(`../assets/img/${icon.img}`)" alt="">
                    <p>{{ icon.title }}</p>
                </li>
            </ul>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.primary-bg {
    background-color: $main_color;
}

.icons-section {
    padding: 2rem 0;

    ul {
        list-style: none;

        img {
            width: 50px;
            margin-right: .5rem;
        }

        p {
            text-transform: uppercase;
            color: $dark_section_text_color;
        }
    }
}
</style>