<template>
  <div class="home">
    <br><br><br>
    <span class="brambora">
      🥔
    </span> <br>  
    <!-- <CountComp/> -->
    <Calendar></Calendar>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import CountComp from '@/components/CountComp.vue';
import Calendar from '../components/Calendar.vue'; // @ is an alias to /src

@Options({
  components: {
    CountComp,
    Calendar
  },
})
export default class HomeView extends Vue {}
</script>
<style lang="scss">
.brambora {
  font-size: 7rem;
}
</style>
