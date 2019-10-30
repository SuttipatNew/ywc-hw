<template>
  <div class="foot-menu">
    <div class="container">
      <div class="foot-menu-item">
        <img id="foot-menu-logo" :src="logo" />
      </div>
      <div class="foot-menu-item">
        <h3>
          ข้อมูลลงทะเบียนประชาชน 
        </h3>
        <p>
          การรับสิทธิ การใช้งานแอปพลิเคชั่น
          <span class="nowrap">
            "เป๋าตัง"
          </span>
          และ
          <span class="nowrap">
            "ถุงเงิน"
          </span>
        </p>
        <p>
          ติดต่อ ชิมช้อปใช้ Call Center by Krungthai โทร.
          <a href="tel:021111144">
            <span class="nowrap">
              0 2111 1144
            </span>
          </a>
        </p>
      </div>
      <div class="foot-menu-item">
        <h3>
          ข้อมูลลงทะเบียนผู้ประกอบการ
        </h3>
        <p>
          เงื่อนไขและวิธีการเข้าร่วมมาตรการฯ
        </p>
        <p>
          ติดต่อ โทร.
          <a href="tel:022706400">
            <span class="nowrap">
              0 2270 6400 กด 7
            </span>
          </a>
        </p>
      </div>
      <div class="foot-menu-item">
        <h3>
          ข้อมูลเที่ยวชิมช้อปใช้
        </h3>
        <p>
          ติดต่อ ททท.
        </p>
        <p>
          โทร.
          <a href="tel:1672">
            <span class="nowrap">
              1672
            </span>
          </a>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
import logo from '../assets/images/footer.png'

export default {
  name: 'FootMenu',
  data() {
    return {
      logo
    }
  }
}
</script>

<style scoped>
div.foot-menu {
  background-color: #FAFAFA;
  font-size: 14px;
  padding: 30px;
}

.foot-menu-item {
  grid-column: span 3;
  text-align: left;
}

#foot-menu-logo {
  width: 108px;
}

h3 {
  margin-top: 24px;
  color: #E6332A;
  font-family: TATSanaSuksa;
}
</style>
