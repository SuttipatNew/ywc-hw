<template>
  <button :class="'hamburger' + (opened ? ' opened' : '')">
    <div v-for="index in 3" :class="'hamburger-line hamburger--' + index" :key="index">
    </div>
  </button>
</template>

<script>
import { EventBus } from '../eventBus.js'

export default {
  name: 'Hamburger',
  data() {
    return {
      opened: false
    }
  },
  created() {
    EventBus.$on('toggle-navbar', () => {
      this.opened = !this.opened
    })
  }
}
</script>

<style scoped>
.hamburger {
  cursor: pointer;
  height: 30px;
  width: 30px;
  border: 0px;
  display: flex;
  justify-content: space-between;
  flex-direction: column;
  padding: 0;
  background-color: transparent;
  outline: none;
  padding: 3px 0;
}

.hamburger-line {
  height: 3px;
  background-color: #333333;
  width: 30px;
  transition: .25s ease-in-out;
}

.opened .hamburger--1 {
  transform: translateY(10.5px) rotate(-45deg);
}

.opened .hamburger--3 {
  transform: translateY(-10.5px) rotate(45deg);
}

.opened .hamburger--2 {
  transform: translateX(-60px);
  background-color: transparent;
}
</style>
