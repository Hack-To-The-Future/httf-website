<template>
  <div class="container">
      <div class="line">
          <p>help&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;displays this message</p>
          <p>play {{`<option>`}}&nbsp;&nbsp;&nbsp;&nbsp;play a game, options: desserts</p>
          <p>exit&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;exits the current action</p>
          <p>dessert check&nbsp;&nbsp;&nbsp;&nbsp;checks the current dessert</p>
          <p>dessert score&nbsp;&nbsp;&nbsp;&nbsp;checks your current score for desserts</p>
          <p>clear&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;clear the console</p>
      </div>
  </div>
</template>

<script>
export default {
  name: 'CliHelp',
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