<script>
export default {
    name: "AppHeader",
    data() {
        return {
            menu: [
                {
                    title: "Characters",
                    url: "/characters",
                    active: false
                },
                {
                    title: "Comics",
                    url: "/comics",
                    active: true
                },
                {
                    title: "Movies",
                    url: "/movies",
                    active: false
                },
                {
                    title: "TV",
                    url: "/tv",
                    active: false
                },
                {
                    title: "Games",
                    url: "/games",
                    active: false
                }
            ]
        }
    }
}
</script>

<template>
    <header>
        <div class="container flex-row justify-between">
            <div class="logo">
                <a href="">
                    <img src="../assets/img/dc-logo.png" alt="Comics DC">
                </a>
            </div>
            <div class="menu">
                <nav>
                    <ul>
                        <li v-for="(link, index) in menu" :key="index">
                            <a :class="{ 'active': link.active }" :href="link.url">{{ link.title }}</a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

header {
    line-height: 70px;

    .logo {
        img {
            height: 70px;
            vertical-align: middle;
        }
    }

    ul {
        list-style: none;
        display: flex;

        li {
            margin: 0 1rem;

            a {
                position: relative;
                display: inline-block;
                text-transform: uppercase;
                text-decoration: none;
                color: $text_color;
                font-weight: 600;
                line-height: inherit;

                &::after {
                    content: "";
                    position: absolute;
                    bottom: 0;
                    left: 0;
                    display: inline-block;
                    width: 100%;
                    height: 0px;
                    background-color: $main-color;
                    transition: height .3s ease;
                }

                &:hover::after,
                &.active::after {
                    height: 5px;
                }
            }
        }
    }
}
</style>