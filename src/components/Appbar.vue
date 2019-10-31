<template>
  <div class="appbar">
    <img :src="logo" />
    <Hamburger @click.native="toggleNavbar" />
  </div>
</template>

<script>
import logo from '../assets/images/footer.png'
import { EventBus } from '../eventBus.js'
import Hamburger from './Hamburger.vue'

export default {
  name: 'Appbar',
  components: {
    Hamburger
  },
  data() {
    return {
      logo
    }
  },
  methods: {
    toggleNavbar() {
      EventBus.$emit('toggle-navbar')
    }
  }
}
</script>

<style scoped>
.appbar {
  height: 64px;
  line-height: 60px;
  align-items: center;
  box-sizing: border-box;
  position: fixed;
  z-index: 11;
  padding: 8px 16px;
  width: 100vw;
  background-color: white;
  top: 0;
  display: flex;
  justify-content: space-between;
}

@media (min-width: 578px) {
  .appbar {
    display: none;
  }
}

img {
  display: block;
  width: 35px;
  height: 48px;
}

.hamburger {
  cursor: pointer;
}
</style>
