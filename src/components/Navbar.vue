<template>
  <ul class="navbar">
    <li v-for="item in items" :key="item.label">
      <a :href="item.href">
        {{ item.label }}
      </a>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'Navbar',
  props: {
    items: Array
  }
}
</script>

<style scoped>

ul {
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
}

a {
  text-decoration: none;
  color: #333333;
  transition: all 0.3s ease-in-out 0s;
}

a:hover {
  color: #213A8F;
}
</style>
