<template>
  <div class="modal-overlay">
    <transition name="slide" appear>
      <div class="modal">
        <h1 class="modal-title">Modal</h1>
        <p>
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Obcaecati deserunt, omnis distinctio maiores excepturi minima placeat expedita molestiae repudiandae consequatur.
        </p>

        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Velit voluptatem, pariatur ipsam reiciendis beatae quaerat eos earum similique laborum quae, aliquam sint. Nemo facere eos accusantium placeat, quibusdam illum ducimus.
        </p>
        <button class="btn-close" @click="$emit('close')"></button>
    </div>

    </transition>  
  </div>
</template>

<script>
 export default {
   data() {
     return {}
   }
  }
</script>

<style lang="scss">
  
.modal-overlay {
  position: fixed;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  z-index: 98;
  background-color: rgba(0, 0, 0, .3);
  
  display: flex;
  justify-content: center;
  align-items: center;

  .modal {
    width: 60%;
    background: #fff;
    padding: 10px;
    border-radius: 10px;
    position: relative;

    .modal-title {
      text-align: center;
      font-size: 30px;
      margin: 1rem 0;
    }

    p {
      font-size: 1rem;
      font-weight: 400;
      line-height: 1.15;
      margin-bottom: 1rem;
    }

    .btn-close {
      cursor: pointer;
      appearance: none;
      outline: none;
      border: none;
      background: none;
      background: linear-gradient(90deg, #43e695 0%, #3bb2b8 75%,  #3bb2b8 100%);
      position: absolute;
      border-radius: 50px;
      color: #fff;

      height: 50px;
      width: 50px;

      font-size: 18px;
      font-weight: 700;
      text-align: center;

      top: -10px;
      right: -10px;
    }
  }

  .slide-enter-active,
  .slide-leave-active {
   transition: transform .5s;
  }

  .slide-enter,
  .slide-leave-to {
    transform: translateY(-50%) translateX(100vw);
  }
}
</style>