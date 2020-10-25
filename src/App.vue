<template>
  <Logo />
  <DessertGame />
  <Footer />
</template>

<script>
import Logo from './components/Logo.vue'
import Footer from './components/Footer.vue'
import DessertGame from './components/DessertGame.vue'

export default {
  name: 'App',
  components: {
    Logo,
    DessertGame,
    Footer
  }
}
</script>

<style lang="postcss">
body {
  @apply bg-gray-900;
}
</style>
