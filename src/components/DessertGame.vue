<template>
  <p class="comment">// Hint: type 'help' to get started...</p>
  <div
    class="outputs"
    v-for="item in lines"
    :key="item.props"
  >
    <component :is="item.type" :extras="item.props"></component>
  </div>
  <CliPrompt @exec="handleCmd" />
</template>

<script>
import rd from "random-desserts"

import CliPrompt from "../components/CliPrompt.vue"
import CliHelp from "../components/CliHelp.vue"
import CliGameStart from "../components/CliGameStart.vue"
import CliMessage from "../components/CliMessage.vue"
import CliError from "../components/CliError.vue"

export default {
  name: 'DessertGame',

  components: {
    CliPrompt,
    CliHelp,
    CliGameStart,
    CliMessage,
    CliError
  },

  data: () => ({
    emoji: '',
    playing: false,
    lines: [],
    score: 0,
    plays: 0,
  }),

  computed: {
    scoreStr() {
      return `${this.score}/${this.plays}`
    }
  },

  methods: {
    handleCmd(cmd) {

      this.lines.push({
        type: CliPrompt,
        props: cmd
      })

      switch (cmd) {
        case 'play':
          if (this.playing) {
            this.lines.push({
              type: CliMessage,
              props: `Game is already in progress... type 'exit' to stop`
            })
          } else {
            this.lines.push({
              type: CliMessage,
              props: 'You need to chose a game, options are: `desserts`'
            })
          }
          break;
        case 'play desserts':
          if (this.playing) {
            this.lines.push({
              type: CliMessage,
              props: `Game is already in progress... type 'exit' to stop`
            })
          } else {
            this.emoji = rd.rollN(1, true)
            this.lines.push({
              type: CliGameStart,
              props: this.emoji
            })
          }
          this.playing = true
          break
        case 'desserts check':
          this.lines.push({
            type: CliMessage,
            props: `Reminder: ${this.emoji}`
          })
          break
        case 'desserts score':
          this.lines.push({
            type: CliMessage,
            props: `Your current score is ${this.scoreStr}`
          })
          break
        case 'exit':
          this.playing = false
          break
        case 'clear':
          this.lines = []
          break
        case 'help':
          this.lines.push({
            type: CliHelp
          })
          break
        default:
          if (this.playing) {
            const altered = cmd.split(' ').map(s => s[0].toUpperCase()+s.substr(1)).join(' ')
            this.plays++
            if (rd.check(this.emoji, altered)) {
              this.playing = false
              this.lines.push({
                type: CliMessage,
                props: `Correct! Your current score is ${this.scoreStr}`
              })
            } else {
              this.lines.push({
                type: CliMessage,
                props: `Sorry, try again...`
              })
            }
          } else {
            lines.push({
              type: CliError,
              props: 'Command not recognised, read help below:'
            })
            lines.push({
              type: CliHelp
            })
          }
          break
      }
    }
  }
}
</script>

<style lang="postcss" scoped>

.comment {
  @apply pl-3 text-gray-700 italic;
}

</style>