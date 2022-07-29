<template>
  <div class="home">
    <br><br><br>
    <span class="brambora">
      🥔
    </span> <br>  
    <CountComp/>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import CountComp from '@/components/CountComp.vue'; // @ is an alias to /src

@Options({
  components: {
    CountComp,
  },
})
export default class HomeView extends Vue {}
</script>
<style lang="scss">
.brambora {
  padding-top: 30rem;
  font-size: 7rem;
}
</style>
