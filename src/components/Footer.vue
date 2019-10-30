<template>
  <div class="footer">
    <ul>
      <li>
        Copyright &copy; 2003-2019
      </li>
      <li>
        ลงทะเบียนเข้าร่วมมาตรการ
      </li>
      <li>
        ขั้นตอนการเข้าร่วมทั้งหมด
      </li>
      <li>
        รายชื่อร้านค้าที่เข้าร่วมรายการ
      </li>
    </ul>
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

ul {
  list-style: none;
  margin: 0;
  text-align: center;
  font-family: TATSanaChon;
  padding: 0px 37px;
  display: grid;
  grid-template-columns: repeat(12, 1fr);
}

li {
  display: inline-block;
  padding: 14px 15px;
  font-weight: bold;
  grid-column: span 3;
  text-align: left;
}
</style>
