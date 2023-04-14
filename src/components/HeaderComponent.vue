<template>
    <header class="d-flex flex-column align-items-center">
        <div>
            <img src="../assets/images/la-molisana-logo.png" alt="Logo Molisana">
        </div>

        <ul class="d-flex gap-2">
            <li v-for="(link, index) in navbar" :key="index">
                <a :href="link.url" :class="{ 'active': link.current }">{{ link.text }}</a>
            </li>
        </ul>
    </header>
</template>

<script>
import { links } from '../data/data.js'
export default {
    name: 'HeaderComponent',
    data() {
        return {
            navbar: links
        }
    },
    created() {

    },
    mounted() {

    }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

ul {
    list-style: none;
    margin: 2.5rem 1rem 4rem;

    li a {
        display: inline-block;
        padding: 1rem;
        text-decoration: none;
        font-weight: 600;

        &.active,
        &:hover {
            background: $lightblue;
        }
    }
}
</style>
