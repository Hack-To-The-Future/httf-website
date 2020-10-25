<template>
  <div class="container">
    <div class="line">
      <p>{{extras}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CliMessage',

  props: {
    extras: String
  }
}
</script>

<style lang="postcss" scoped>

p {
  @apply text-gray-100
}

.container {
  @apply pl-1 w-screen;
}

.line {
  @apply ml-10;
}

</style>