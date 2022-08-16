<template>
  <div>
    <div class="modal-mask">
      <div class="modal-wrapper">
        <div class="modal-container">
              <button class="modal-default-button" @click="$emit('close')">
            Hotovo
          </button>
          <br><br><br>
          <div class="modal-header" v-html="string"></div>
          <br />

      
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { prop, Vue } from "vue-class-component";

class Props {
  string: string = prop({
    required: true,
  });
}
export default class ModalComponent extends Vue.with(Props) {}
</script>

<style lang="scss" scoped>
.modal-mask {
  position: fixed;
  z-index: 9998;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  display: table;
  transition: opacity 0.3s ease;
}

.modal-wrapper {
  display: table-cell;
  vertical-align: middle;
}

.modal-container {
  max-width: 30rem;
  max-height: 100vh;
  overflow: auto;
  margin: 0px auto;
  padding: 20px 30px;
  background-color: #fff;
  border-radius: 2px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.33);
  transition: all 0.3s ease;
  font-family: Helvetica, Arial, sans-serif;
}

.modal-header h3 {
  margin-top: 0;
  color: #42b983;
}

.modal-body {
  margin: 20px 0;
}

.modal-default-button {
  float: right;
}
</style>
