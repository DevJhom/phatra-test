<script>
import MainLogo from "../ui/MainLogo.vue";
import FooterLogos from "./FooterLogos.vue";

export default {
  name: "TheFooter",
  components: {
    MainLogo,
    FooterLogos,
  },
};
</script>

<template>
  <footer>
    <div class="footer-bg">
      <div class="container pt-4">
        <div class="row">
          <div class="col-4 d-flex flex-column">
            <nuxt-link to="/">
              <main-logo></main-logo>
            </nuxt-link>
            <span class="company-name">บริษัท ทุนภัทร จำกัด (มหาชน)</span>
            <span class="address">
              ชั้น 9 อาคารสำนักงานเมืองไทย-ภัทร 1 252/6 ถนนรัชดาภิเษก
              แขวงห้วยขวาง กรุงเทพมหานคร 10310
            </span>
          </div>
          <div class="col-2 d-flex flex-column">
            <span class="menu-title">เมนู</span>
            <ul class="list-unstyled menus">
              <li>
                <a href="#!">รู้จัก บลจ.ภัทร</a>
              </li>
              <li>
                <a href="#!">เกี่ยวกับเรา</a>
              </li>
              <li>
                <a href="#!">ติดต่อเรา</a>
              </li>
              <li>
                <a href="#!">คำถามที่พบบ่อย</a>
              </li>
              <li>
                <a href="#!">สมัครงาน</a>
              </li>
              <li>
                <a href="#!">Links</a>
              </li>
            </ul>
          </div>
          <div class="col-2 d-flex flex-column">
            <span class="menu-title">เมนู</span>
            <ul class="list-unstyled menus">
              <li>
                <a href="#!">รู้จัก บลจ.ภัทร</a>
              </li>
              <li>
                <a href="#!">เกี่ยวกับเรา</a>
              </li>
              <li>
                <a href="#!">ติดต่อเรา</a>
              </li>
              <li>
                <a href="#!">คำถามที่พบบ่อย</a>
              </li>
              <li>
                <a href="#!">สมัครงาน</a>
              </li>
              <li>
                <a href="#!">Links</a>
              </li>
            </ul>
          </div>
          <div class="col-4 d-flex flex-column">
            <span class="menu-title">ติดต่อเรา</span>
            <div class="d-flex justify-content-start mb-1">
              <img class="icons" src="@/assets/icons/ic-tel.svg" />
              <span class="contact">(66) 2305 9800</span>
            </div>
            <div class="d-flex justify-content-start mb-1">
              <img class="icons" src="@/assets/icons/ic-fax.svg" />
              <span class="contact">(66) 2305 9800</span>
            </div>
            <div class="d-flex justify-content-start mb-1">
              <img class="icons" src="@/assets/icons/ic-mail.svg" />
              <span class="contact email">customerservice@phatraasset.com</span>
            </div>
            <div class="d-flex">
              <a href="https://www.facebook.com/" target="_blank">
                <img class="social" src="@/assets/icons/facebook.svg" />
              </a>
              <a href="https://www.twitter.com/" target="_blank">
                <img class="social" src="@/assets/icons/twitter.svg" />
              </a>
              <a href="https://www.youtube.com/" target="_blank">
                <img class="social" src="@/assets/icons/youtube.svg" />
              </a>
            </div>
          </div>
        </div>
        <hr style="margin-top: 0" />
        <div class="container text-center">
          <div class="d-flex justify-content-between">
            <div class="d-flex">
              <small class="copyright">แผนผังเว็บไซต์</small>
              <div class="line"></div>
              <small class="copyright">ข้อตกลงและเงื่อนไข</small>
              <div class="line"></div>
              <small class="copyright">นโยบายข้อมูลส่วนตัว</small>
            </div>
            <div class="d-flex">
              <small class="copyright">
                @2019 Phatra A© สงวนลิขสิทธิ์ 2562 บริษัทหลักทรัพย์จัดการกองทุน
                ภัทร จำกัดsset All rights reserved.
              </small>
            </div>
          </div>
        </div>
      </div>
    </div>
    <footer-logos></footer-logos>
  </footer>
</template>

<style scoped>
* {
  color: #fff;
  font-stretch: normal;
  font-style: normal;
  letter-spacing: normal;
}

.footer-bg {
  width: 100%;
  height: auto;
  background-image: linear-gradient(to bottom, #6f6eb2 3%, #352c64 106%);
}

a {
  text-decoration: none;
}

a:hover {
  color: #211e19;
}

.company-name {
  margin: 27px 0 10px 0;
  font-family: Kanit;
  font-size: 1.375rem;
  font-weight: 500;
  line-height: 1.36;
}

.address {
  margin: 10px 0 46px 0;
  max-width: 308px;
  font-family: Tahoma;
  font-size: 1rem;
  font-style: normal;
  line-height: 1.56;
}

.menu-title {
  height: 21px;
  margin: 8px 0 20px 0;
  font-family: Quark;
  font-size: 24px;
  font-weight: bold;
  line-height: 0.88;
}

.menus {
  font-family: Tahoma;
  font-size: 1rem;
  line-height: 1.75;
  color: #fff;
}

.icons {
  width: 22px;
  height: 23px;
  margin: 0 27px 21px 0;
  object-fit: contain;
}

.contact {
  font-family: Tahoma;
  font-size: 1rem;
}

.social {
  width: 44px;
  height: 44px;
  margin: 0 9px 0 0;
  object-fit: contain;
}

.copyright {
  margin-bottom: 20px;
  opacity: 0.5;
  font-family: Tahoma;
  font-size: 0.8rem;
  font-weight: normal;
  line-height: normal;
  letter-spacing: normal;
  color: #cfcbeb;
}

.line {
  width: 1px;
  height: 18px;
  margin: 0 10px;
  opacity: 0.5;
  border: 1px solid #cfcbeb;
}

@media (max-width: 912px) {
  .company-name,
  .menu-title {
    font-size: 12px;
  }

  .address,
  .menus,
  .contact,
  .copyright {
    font-size: 8px;
  }

  .email {
    width: 100px;
    word-break: break-all;
  }

  .icons {
    width: 12px;
    height: 12px;
    margin: 0 5px;
  }

  .social {
    width: 22px;
    height: 22px;
  }
}
</style>
