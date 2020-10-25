<template>
  <div class="container">
    <div class="line">
      <p class="text-xs md:text-lg">&nbsp;&nbsp;&nbsp;&nbsp;____&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;__&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</p>
      <p class="text-xs md:text-lg">&nbsp;&nbsp;&nbsp;/&nbsp;__&nbsp;\____&nbsp;_____&nbsp;&nbsp;____/&nbsp;/___&nbsp;&nbsp;____&nbsp;___&nbsp;</p>
      <p class="text-xs md:text-lg">&nbsp;&nbsp;/&nbsp;/_/&nbsp;/&nbsp;__&nbsp;`/&nbsp;__&nbsp;\/&nbsp;__&nbsp;&nbsp;/&nbsp;__&nbsp;\/&nbsp;__&nbsp;`__&nbsp;\</p>
      <p class="text-xs md:text-lg">&nbsp;/&nbsp;_,&nbsp;_/&nbsp;/_/&nbsp;/&nbsp;/&nbsp;/&nbsp;/&nbsp;/_/&nbsp;/&nbsp;/_/&nbsp;/&nbsp;/&nbsp;/&nbsp;/&nbsp;/&nbsp;/</p>
      <p class="text-xs md:text-lg">/_/&nbsp;|_|\__,_/_/&nbsp;/_/\__,_/\____/_/&nbsp;/_/&nbsp;/_/&nbsp;</p>
      <p class="text-xs md:text-lg">&nbsp;&nbsp;&nbsp;&nbsp;____&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;__&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</p>
      <p class="text-xs md:text-lg">&nbsp;&nbsp;&nbsp;/&nbsp;__&nbsp;\___&nbsp;&nbsp;_____________&nbsp;&nbsp;_____/&nbsp;/______</p>
      <p class="text-xs md:text-lg">&nbsp;&nbsp;/&nbsp;/&nbsp;/&nbsp;/&nbsp;_&nbsp;\/&nbsp;___/&nbsp;___/&nbsp;_&nbsp;\/&nbsp;___/&nbsp;__/&nbsp;___/</p>
      <p class="text-xs md:text-lg">&nbsp;/&nbsp;/_/&nbsp;/&nbsp;&nbsp;__(__&nbsp;&nbsp;|__&nbsp;&nbsp;)&nbsp;&nbsp;__/&nbsp;/&nbsp;&nbsp;/&nbsp;/_(__&nbsp;&nbsp;)&nbsp;</p>
      <p class="text-xs md:text-lg">/_____/\___/____/____/\___/_/&nbsp;&nbsp;&nbsp;\__/____/&nbsp;&nbsp;</p>
    </div>
    <div class="line">
      <br/>
      <p class="msg text-xs md:text-lg">Guess the name of the dessert from it's emoji!</p>
      <p class="msg text-xs md:text-lg">Your random dessert is:</p>
      <p class="pl-10 md:text-4xl">{{extras}}</p>
      <p class="msg text-xs md:text-lg">Type your guess into the terminal...</p>
      
    </div>
  </div>
</template>
                  

<script>
export default {
  name: 'CliGameStart',
  props: {
    extras: {
      type: String,
      default: ''
    }
  }
}
</script>

<style lang="postcss" scoped>

p {
  @apply text-green-400 font-bold
}

.msg {
  @apply text-teal-600
}

.container {
  @apply pl-1 w-screen;
}

.line {
  @apply ml-10;
}

</style>