<template>
    <div class="container nav_bar">
        <div class="nav_logo">
            <router-link :to="{name: 'home'}">
                <div class="nav_thumb"></div>
            </router-link>
        </div>

        <ul class="nav_menu">
            <li class="nav_item">
                <router-link :to="{name:'home'}"><span class="nav_num">01.</span> Home</router-link>
            </li>
            <li class="nav_item">
                <router-link :to="{name:'portfolio'}"><span class="nav_num">02.</span> Portfolio</router-link>
            </li>
            <li class="nav_item">
                <router-link :to="{name:'about'}"><span class="nav_num">03.</span> About</router-link>
            </li>
            <li class="nav_item">
                <span class="nav_num">04.</span> Contacts
            </li>

            <li class="nav_item">
                <div class="btn-container">
                    <div class="btn">
                        <a href="curriculm">Download CV</a>                    
                    </div>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        mounted() {
            setTimeout(() => {
                document.querySelector('.nav_bar').style.opacity = 1
            }, 1000)
        }
    }
</script>

<style lang="scss" scoped>
@use '../src/styles/partials/resets' as *;
@use '../src/styles/partials/variables' as *;
@use '../src/styles/partials/_button.scss' as*;
.nav_bar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 2rem;
    opacity: 0;
    transition: opacity 0.5s linear;

    .nav_logo {
        width: 30px;

        .nav_thumb {
            background-color: red;
            height: 30px;
        }
    }

    .nav_menu {
        display: flex;
        align-items: center;
        justify-content: space-around;
        gap: 1rem;
        font-size: 1rem;
        font-family: 'Roboto Mono', monospace;

        .nav_item {
            color: $text;
            .nav_num {
                color: $links;
            }
        }

        .nav_item:hover {
            color: $links;
        }
    }
}
</style>