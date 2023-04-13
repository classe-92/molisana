<template>
    <footer>
        <img src="../assets/images/la-molisana-logo.png" alt="Logo Molisana">
        <ul v-for="(list, index) in lists" :key="index">
            <li>{{ list.title }}</li>
            <li v-for="(item, i) in list.links" :key="i">
                <a :href="item.url">{{ item.text }}</a>
            </li>
        </ul>

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
footer {
    background-image: url('../assets/images/footer-montagne-bottom.jpg');
    background-repeat: no-repeat;
    background-position: bottom;
}
</style>