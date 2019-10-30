<template>
  <div class="call">
    <div v-for="item in items" :key="item.number">
      <a :href="'tel:' + item.number">
        <img :src="item.img"/>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Call',
  data() {
    return {
      items: [
        {
          number: '021111144',
          img: require('../assets/images/Banner_KTB_SQ.png')
        },
        {
          number: '022706400',
          img: require('../assets/images/Banner_CGD_Sq.png')
        },
        {
          number: '1672',
          img: require('../assets/images/Banner_TAT_Hotline_Sq.png')
        }
      ],
    }
  }
}
</script>

<style scoped>

.call {
  margin: 120px 0;
  grid-column: span 12;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-column-gap: 15px;
}

.call img {
  width: 80%;
}

</style>
