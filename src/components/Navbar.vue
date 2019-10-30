<template>
  <ul :class="'navbar' + (expanded ? ' expanded' : '')">
    <li v-for="item in items" :key="item.label">
      <a :href="item.href">
        {{ item.label }}
      </a>
    </li>
  </ul>
</template>

<script>
import { EventBus } from '../eventBus.js'

export default {
  name: 'Navbar',
  props: {
    items: Array,
  },
  data() {
    return {
      expanded: false
    }
  },
  created() {
    EventBus.$on('toggle-navbar', () => {
      this.expanded = !this.expanded
    })
  }
}
</script>

<style scoped>

ul {
  height: 60px;
  box-sizing: border-box;
  list-style: none;
  margin: 0;
  padding-left: 0px;
  text-align: center;
  background-color: white;
  width: 100vw;
  position: fixed;
  padding-top: 5px;
  top: 0px;
  font-family: TATSanaChon;
  box-shadow: rgba(0, 0, 0, 0.0980392) 0px 4px 10px 0px;
  z-index: 10;
}

li {
  display: inline-block;
  padding: 14px 15px;
  font-size: 14px;
  font-weight: bold;
  color: #333333;
}

a {
  text-decoration: none;
  transition: all 0.3s ease-in-out 0s;
}

a:hover {
  color: #213A8F;
}

@media (max-width: 577px) {
  ul {
    padding-top: 60px;
    transition: height .35s ease;
    overflow: hidden;
  }
  li {
    display: block;
    text-align: right;
    font-family: TATSanaSuksa;
    color: rgba(0,0,0,.5);
    font-size: 16px;
    font-weight: normal;
  }
  .expanded {
    height: 237.6px;
  }
}
</style>
