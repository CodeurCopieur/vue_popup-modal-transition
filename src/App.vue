<template>
  <div id="app">
    <button class="btn-modal" @click="showModal = !showModal">Show Modal</button>

    <transition name="fade" appear>
      <Modal v-if="showModal" @close="showModal = !showModal" />
    </transition>
    
  </div>
</template>

<script>
import Modal from './components/modal.vue'

export default {
  name: 'App',
  components: {
    Modal
  },
  data() {
    return {
      showModal: false
    }
  }
}
</script>

<style lang="scss">
*, ::before, ::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  color: #2c3e50;
  width: 100vw;
  min-height: 100vh;

  display: flex;
  justify-content: center;
  align-items: center;

  position: relative;

  .btn-modal {
   cursor: pointer;
   appearance: none;
   outline: none;
   border: none;
   background: none;
   background: linear-gradient(90deg, #3bb2b8 0%, #3bb2b8 25%, #43e695 100%);
   
   padding: 15px 25px;
   border-radius: 8px;
   color: #fff;

   font-size: 18px;
   font-weight: 700;

   box-shadow: 3px 3px rgba(0, 0, 0, .4);
   transition: .4s ease-out;

   &:hover {
     box-shadow: 6px 6px rgba(0, 0, 0, .6);
   }
 }

 .fade-enter-active,
 .fade-leave-active {
   transition: opacity .5s;
 }

 .fade-enter,
 .fade-leave-to {
   opacity: 0;
 }
}

</style>
