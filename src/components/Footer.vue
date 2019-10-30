<template>
  <div class="footer">
    <div class="container">
      <div class="footer-item">
        Copyright &copy; 2003-2019
      </div>
      <div class="footer-item">
        ลงทะเบียนเข้าร่วมมาตรการ
      </div>
      <div class="footer-item">
        ขั้นตอนการเข้าร่วมทั้งหมด
      </div>
      <div class="footer-item">
        รายชื่อร้านค้าที่เข้าร่วมรายการ
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer'
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
</style>
