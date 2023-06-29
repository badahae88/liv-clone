<template>
  <Modal
    @closeModal="showModal=false"
    :showModal='showModal'
    :showItem='showItem'
  />

  <Menu
    @closeBanner="openBanner=false"
    :openBanner="openBanner"
  />


  <Card v-for="item in items" :key="item"
    @click="showModal=true; showItem=item;"
    :item="item"
  />

  <Footer/>
</template>

<script>
import items from './items';
import Menu from './components/Menu.vue'
import Card from './components/Card.vue'
import Modal from './components/Modal.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  data(){
    return {
      items: items,
      openBanner: true,
      showModal: false,
      showItem: {},
    }
  },
  components: {
    Menu,
    Card,
    Modal,
    Footer,
  }
}
</script>

<style>
.app{
  text-align: center;
}


</style>
