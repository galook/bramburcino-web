<template>
<ModalComponent v-if="showModal" :string="string" @close="showModal = false" />
  <h2 class="calendar">Brambůrčin Kalendáč</h2>
  <span>Plný zajímavých věcí</span>
  <br><br><br>
  <div class="days">

    <div @click="display(day)" v-for="day in days" :key="day">
      <button>{{ day + 1 }}</button>
    </div>

  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import axios from "axios"
import ModalComponent from "./ModalComponent.vue"

@Options({
  components: {
    ModalComponent
  }
})
export default class Calendar extends Vue {
  showModal = false
  days = [...Array(31).keys()];
  string = "Nahlaš chybu AX1 Matýskovi"

  public async display(day: string) {
    const result = await axios.get("https://bramburcino-day-access.stamina.green" + Number(day + 1))
    console.log(result);
    console.log(this.days);

    this.showModal = true
    this.string = result.data
    
    
    
  }
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
