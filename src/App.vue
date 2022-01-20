<template>
  <v-app style="font-family: IRYekan;">
    <b-row dir="rtl">
      <!-- <b-navbar toggleable="lg" style="background-color: #0d5671">
        <div>
          <b-navbar variant="faded" type="light">
            <b-navbar-brand class="mr-15" href="/">
              <img
                class="mt-0 mb-0 pt-0 pb-0"
                width="55px"
                height="55px"
                src="@/assets/talagram.png"
                alt="طلاگرام"
              />
            </b-navbar-brand>
          </b-navbar>
        </div>
        <b-navbar-brand>
          <router-link to="/">
            <p style="color: #f5d438; text-shadow: 3px 3px 7px black">
              طلاگرام
            </p>
          </router-link>
        </b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse class="mr-15" id="nav-collapse" is-nav>
          <b-navbar-nav>
            <b-nav-item class="ml-2" href="#">
              <h6>
                <b style="color: #bea44d"> </b>
              </h6>
            </b-nav-item>

            <b-nav-item class="ml-2">
              <router-link to="/about"
                ><h6>
                  <b style="color: #efede9"> محاسبه قیمت حباب </b>
                </h6></router-link
              >
            </b-nav-item>

            <b-nav-item class="ml-2" href="/ShowPrice">
              <h6><b style="color: #efede9"> قیمت انلاین </b></h6>
            </b-nav-item>

            <b-nav-item class="ml-2" href="/MainChart">
              <h6><b style="color: #efede9"> نمودار </b></h6>
            </b-nav-item>

            <b-nav-item class="ml-2" href="ShowPrice2">
              <h6>
                <b style="color: #efede9"> قیمت انلاین- 2 </b>
              </h6>
            </b-nav-item>

            <b-nav-item class="ml-2" href="ShowPrice3">
              <h6><b style="color: #efede9"> قیمت انلاین- 3 </b></h6>
            </b-nav-item>

        
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>  -->
    </b-row>
    <router-view />

    <!-- <b-row class="footer" align="center" dir="rtl">
      <hr />

      <b-col>
        <div class="container">
          <h5>
            <b style="color: #efede9; text-shadow: 3px 3px 7px black">
              لینک های مفید
            </b>
          </h5>
          <br />
          <div class="place">
            <h6>
              <a href="https://ex.ebidar.com/v-533">
                <li class="place">اقتصاد بیدار</li>
              </a>
            </h6>

            <h6 class="place">
              <a style="color: black" href="https://t.me/tahlilonline_com">
                <li class="place">تحلیل انلاین</li>
              </a>
            </h6>

            <h6 class="place">
              <a style="color: black" href="https://t.me/tahlilonline_com">
                <li class="place">باشگاه زمرد</li>
              </a>
            </h6>
          </div>
        </div>
      </b-col>

      <b-col>
        <div>
          <h5 class="">
            <b style="color: #efede9; text-shadow: 3px 3px 7px black">
              راه های ارتباطی
            </b>
          </h5>
          <br />
          <div>
            <h6 style="color: #a5b9bd">
              شیراز، خیابان قصرالدشت، چهارراه ملاصدرا، مرکز خرید طلا و جواهر
              پارس، طبقه همکف واحد 29
            </h6>
          </div>

          <div class="place">
            <h3>
              <a href="tel:07132301858">
                <p class="place">071-32301858</p>
              </a>
            </h3>
            <h3>
              <a href="tel:09171092419">
                <p class="place">09171092419</p>
              </a>
            </h3>
          </div>

          <br />
        </div>
        <div class="place1 container">
          <a class="place1 ml-1" href="https://t.me/talagram_chnl">
            <img class="place1" src="@/assets/tel3.png" />
          </a>

          <a
            class="place1 ml-1"
            href="https://instagram.com/tahlilonline_com?utm_medium=copy_link"
          >
            <img src="@/assets/ins.png" />
          </a>

          <a class="place1 ml-2" href="https://www.aparat.com/tahlilonline.com">
            <img src="@/assets/apa.png" />
          </a>

          <a
            class="place1"
            href="https://www.youtube.com/channel/UCo0Q1Re84VCVjemnr6-uN_g"
          >
            <img src="@/assets/you.png" />
          </a>
        </div>
      </b-col>
      <hr />
      <br />

      <h6>
        <v-icon style="font-size: 20px"> copyright </v-icon>

        کلیه حقوق متعلق به گروه مالی زمرد ‌می ‌باشد.
      </h6>
      <br />

      <br />
    </b-row> -->
  </v-app>
</template>
 
 
 
 <script>
export default {
  created() {},
};
</script>
 
 
<style scoped lang="scss">
@font-face {
  font-family: "IRYekan";
  src: local("IRYekan"), url(./font/IRYekan.ttf) format("truetype");
}




a:link {
  text-decoration: none;
  background-color: none !important;
}







</style>
