<template>
  <Logo />
  <Footer />
</template>

<script>
import Logo from './components/Logo.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Logo,
    Footer
  }
}
</script>

<style lang="postcss">
body {
  @apply bg-gray-900;
}
</style>
