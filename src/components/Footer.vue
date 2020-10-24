<template>
  <div class="container">
    <div class="content">
      <span>Find out more here:</span>
        <a href="https://github.com/Hack-To-The-Future">
          <img src="../assets/GitHub-Mark-Light-64px.png" />
        </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style lang="postcss" scoped>

.container {
  @apply absolute bottom-0 flex
}

.content {
  @apply mx-auto flex flex-row
}

span {
  @apply my-auto
}

img {
  @apply h-6 ml-2 mb-2
}

</style>