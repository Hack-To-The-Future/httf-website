<template>
  <div class="container">
    <div class="line">
      <p>{{extras}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CliError',

  props: {
    extras: String
  }
}
</script>

<style lang="postcss" scoped>

p {
  @apply text-red-700
}

.container {
  @apply pl-1 w-screen;
}

.line {
  @apply ml-10;
}

</style>