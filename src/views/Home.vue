<template>
  <div class="home">
    <Modal @close="toggleModal" :modalActive="modalActive">
      <div class="modal-content">
        <h4>Hello from</h4>
        <h1><a href="https://hokify.at" style="color:white">🎆 Hokify 🎆</a></h1>
      </div>
    </Modal>
    <button @click="toggleModal" type="button">Say Hello</button>
  </div>
</template>

<script>
import Modal from "@/components/Modal.vue";
import { ref } from "vue";
export default {
  name: "Home",
  components: {
    Modal,
  },
  setup() {
    const modalActive = ref(false);
    const toggleModal = () => {
      modalActive.value = !modalActive.value;
    };
    return { modalActive, toggleModal };
  },
};
</script>

<style lang="scss" scoped>
.home {
  
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  .modal-content {
      color: #fff;
    display: flex;
    flex-direction: column;
    h1,
    p {
      margin-bottom: 16px;
    }
    h1 {
      font-size: 32px;
    }
    p {
      font-size: 18px;
    }
  }
}
</style>