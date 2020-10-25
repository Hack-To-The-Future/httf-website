<template>
  <div class="container">
    <form @submit.prevent="onSubmit">
      <div class="line">
        <span class="prompt">$</span>
        <input class="cli focus:outline-none" type="text" v-model="cmd" >
      </div>
      <input type="submit" hidden />
    </form>
  </div>
</template>

<script>


export default {
  name: 'CliPrompt',

  props: {
    extras: {
      type: String,
      default: ''
    }
  },

  data: () => ({
    cmd: ''
  }),

  mounted() {
    this.cmd = this.$props.extras
  },

  methods: {
    onSubmit: function () {
      this.$emit('exec', this.cmd)
      this.cmd = ''
    }
  }
}
</script>

<style lang="postcss" scoped>

.prompt {
  @apply text-gray-100 mr-2;
}

.container {
  @apply pl-1 w-screen;
}

.line {
  @apply flex;
}

.cli {
  @apply bg-gray-900 w-full;
}

</style>