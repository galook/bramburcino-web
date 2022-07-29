<template>
  <div class="home">
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
  font-size: 15rem;
}
</style>
