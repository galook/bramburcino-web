<template>
  <h2 class="calendar">Brambůrčin Klanendář</h2>
  <span>Plný zajímavých věcí</span>
  <br><br><br>
  <div class="days">

    <div v-for="day in days" :key="day">
      <button>{{ day + 1 }}</button>
    </div>

  </div>
</template>

<script lang="ts">
import { Vue } from "vue-class-component";

export default class Calendar extends Vue {
  days = [...Array(31).keys()];
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.days {
  width: 21rem;
  margin: auto;
  display: grid;
  gap: 15px;
  grid-template-columns: repeat(7, auto)
}
button {
  width: 2rem;
  height: 2rem
  }
</style>
