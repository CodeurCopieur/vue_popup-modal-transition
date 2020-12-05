<template>
  <div class="modal-overlay">
    <h1>modal</h1>
  </div>
</template>

<script>
 export default {
   data() {
     return {}
   }
  }
</script>

<style>
  
.modal-overlay {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  z-index: 98;
  background-color: rgba(0, 0, 0, .3);
}
</style>