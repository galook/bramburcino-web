<template>
  <vue-countdown
    :time="timeRem"
    v-slot="{ days, hours, minutes, seconds }"
  >
  <h1>{{days}} dní</h1> <h2>{{hours.toLocaleString('en-US', { minimumIntegerDigits: 2})}}:{{minutes.toLocaleString('en-US', { minimumIntegerDigits: 2})}}:{{seconds.toLocaleString('en-US', { minimumIntegerDigits: 2})}}</h2>
  </vue-countdown>
</template>

<script lang="ts">
import { Vue } from "vue-class-component";

export default class Count extends Vue {
    dateNow = new Date()
    dateEnd = new Date("August 12 2022")
    get timeRem() {
        return  this.dateEnd.getTime() - this.dateNow.getTime()
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
