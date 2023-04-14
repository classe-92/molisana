<template>
    <main>
        <section class="container">
            <div class="row">

                <CardComponent :image="pasta.src" :title="pasta.titolo" v-for="(pasta, index) in pastas" :key="index" />

            </div>
        </section>
    </main>
</template>

<script>
import { products } from '../data/data.js';
import CardComponent from './CardComponent.vue';
export default {
    name: 'MainComponent',
    components: {
        CardComponent
    },
    data() {
        return {
            pastas: [...products]
        }
    }

}
</script>

<style lang="scss" scoped>
main {
    background-image: url('../assets/images/fondo-pag-speciali.jpg');
}
</style>