<template>
  <div class="footer">
    <div class="container">
      <div class="footer-item">
        Copyright &copy; 2003-2019
      </div>
      <div class="footer-item" v-for="index in 3" :key="index">
        <a :href="items[index - 1].href">
          {{ labels[index - 1] }}
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer',
  props: {
    items: Array
  },
  data() {
    return {
      labels: [
        'ลงทะเบียนเข้าร่วมมาตรการ',
        'ขั้นตอนการเข้าร่วมทั้งหมด',
        'รายชื่อร้านค้าที่เข้าร่วมรายการ'
      ]
    }
  }
}
</script>

<style scoped>
div.footer {
  background-color: rgb(33, 58, 143);
  color: white;
  font-size: 14px;
}

.footer-item {
  font-family: TATSanaSuksaBold;
  padding: 8px 0px;
  grid-column: span 3;
  text-align: left;
}

@media (max-width: 577px) {
  div.footer {
    padding: 15px 0px;
  }

  .footer-item {
    grid-column: span 12;
    padding: 0.5rem 2rem;
    font-size: 12px;
  }
}
</style>
