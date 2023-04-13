<template>
    <footer>
        <div class="cols container">
            <a href="#" class="logo">
                <img src="../assets/images/la-molisana-logo.png" alt="La Molisana">
            </a>
            <ul v-for="(list, index) in lists" :key="index" class="footer-links">
                <li>{{ list.title }}</li>
                <li v-for="(item, i) in list.links" :key="i">
                    <a :href="item.url">{{ item.text }}</a>
                </li>
            </ul>
            <!-- <FooterMenu v-for="(list, index) in lists" :key="index" :item="menu" /> -->

        </div>
    </footer>
</template>

<script>
import { menu } from '../data/data.js';
export default {
    name: 'FooterComponent',
    data() {
        return {
            lists: menu
        }
    }

}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

footer {
    width: 100%;
    padding-top: 3rem;
    background-image: url('../assets/img/footer-montagne-bottom.jpg');
    background-repeat: no-repeat;
    background-position: bottom;
    padding-bottom: 1rem;

    .cols {
        display: flex;

        .logo,
        .footer-links {
            flex-basis: calc(100% / 3);
            padding: 0 1rem;
        }

        h4 {
            text-transform: uppercase;
            font-size: 1.25em;
            font-weight: 600;
            margin-bottom: 1rem;
            color: $bluetext;
        }

        ul {
            list-style: none;

            li a {
                display: inline-block;
                margin-bottom: 0.25rem;
                text-decoration: none;
                font-size: 0.875em;

                &:hover {
                    color: $bluetext;
                }
            }
        }
    }
}
</style>