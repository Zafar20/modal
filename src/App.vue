<template>
    <div class="wrapper">
      <div class="wrapper-content">
        <section>
          <div class="container">
            <button @click="modalFirst = !modalFirst" class="btn btnPrimary">Show First Modal</button>
            <Modal 
              title="First Modal"
              v-if="modalFirst"
              @close="modalFirst = !modalFirst">
              <div slot="body">
                <p>Text by Zafar</p>
                <button class="btn btnPrimary">Well done</button>
              </div>
            </Modal>
          </div>
        </section>
      </div>
    </div>
</template>

<script>

import Modal from '@/components/Modal.vue';

export default {
  components:{
    Modal
  },
  data() {
    return {
      modalFirst: false
    }
  }
}
</script>

<style>

</style>
