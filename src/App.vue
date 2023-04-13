<template>
  <div class="container">
    <h1>Ciao</h1>

    <HeaderComponent />
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
export default {
  name: 'App',
  components: {
    HeaderComponent
  }

}
</script>

<style lang="scss" scoped>
h1 {
  color: green
}
</style>