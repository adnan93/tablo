<template>
  <div class="d">
    <div>
      <b-row class="up">
        <b-row dir="rtl">
          <b-col cols="1"> </b-col>

          <b-col cols="10">
            <b-row class="hcolor mt-2">
              <b-col align="right" cols="5">
                <b-row>
                  <h5 class="hcolor">بورس سکه و آبشده شرکت زمزد</h5>
                </b-row>
                <b-row>
                  <h5 class="hcolor">تاریخ:{{ today }}</h5>
                </b-row>
              </b-col>

              <b-col align="center" cols="2">
                <img
                  class="mt-0 mb-0 pt-0 pb-0"
                  width="65px"
                  height="65px"
                  src="@/assets/talagram.png"
                  alt="طلاگرام"
                />
              </b-col>
              <b-col cols="1"> </b-col>

              <b-col align="left" cols="4">
                <b-row>
                  <h3 class="hcolor">
                    0987798462

                    <v-icon style="font-size: 35px; color: black"
                      >whatsapp</v-icon
                    >
                  </h3>
                </b-row>

                <b-row>
                  <h3 class="hcolor">
                    0987798462

                    <v-icon style="font-size: 30px; color: black">call</v-icon>
                  </h3>
                </b-row>

                <!-- <b-row>
                  <h1> {{ time }}</h1>
                </b-row> -->
              </b-col>
            </b-row>
          </b-col>

          <b-col cols="1"> </b-col>
        </b-row>
      </b-row>

      <b-row dir="rtl" class="down pr-0 mr-0">
        <b-col cols="1"></b-col>

        <b-col cols="10">
          <b-row class="mt-6">
            <b-col>
              <b-card border-variant="dark" align="center">
                <template #header>
                  <div style="text-align: center">
                    <p style="color: black">یک مثقال طلای</p>
                  </div>
                </template>

                <b-card-text>
                  <h3>
                    {{ mesghalRiyal }}
                    0
                  </h3>
                </b-card-text>
              </b-card>
            </b-col>
            <b-col>
              <b-card border-variant="dark" header="ربع سکه" align="center">
                <template #header>
                  <div style="text-align: center">
                    <p style="color: black">ربع سکه</p>
                  </div>
                </template>

                <b-card-text>
                  <h3>
                    {{ robPrice }}
                  </h3>
                </b-card-text>
              </b-card>
            </b-col>
            <b-col>
              <b-card border-variant="dark" align="center">
                <template #header>
                  <div style="text-align: center">
                    <p style="color: black">سکه یک گرمی</p>
                  </div>
                </template>
                <b-card-text>
                  <h3>{{ sekeGeramiPrice }}</h3>
                </b-card-text>
              </b-card>
            </b-col>
          </b-row>
               <br>

          <b-row class="mt-6">
            <b-col>
              <b-card border-variant="dark" align="center">
                <template #header>
                  <div style="text-align: center">
                    <p style="color: black">نیم سکه</p>
                  </div>
                </template>

                <b-card-text>
                  <h3>
                    {{ nimPrice }}
                  </h3>
                </b-card-text>
              </b-card>
            </b-col>
            <b-col>
              <b-card border-variant="dark" align="center">
                <template #header>
                  <div style="text-align: center">
                    <p style="color: black">انس</p>
                  </div>
                </template>

                <b-card-text>
                  <h3>
                    {{ ons }}
                  </h3>
                </b-card-text>
              </b-card>
            </b-col>
            <b-col>
              <b-card border-variant="dark" header="دلار" align="center">
                <template #header>
                  <div style="text-align: center">
                    <p style="color: black">دلار</p>
                  </div>
                </template>
                <b-card-text>
                  <h3>{{ dollar }}</h3>
                </b-card-text>
              </b-card>
            </b-col>
          </b-row>
          <br>

          <b-row class="mt-6">
            <b-col>
              <b-card border-variant="dark" align="center">
                <template #header>
                  <div style="text-align: center">
                    <p style="color: black">نیم سکه</p>
                  </div>
                </template>

                <b-card-text>
                  <h3>
                    {{ nimPrice }}
                  </h3>
                </b-card-text>
              </b-card>
            </b-col>
            <b-col>
              <b-card border-variant="dark" align="center">
                <template #header>
                  <div style="text-align: center">
                    <p style="color: black">انس</p>
                  </div>
                </template>

                <b-card-text>
                  <h3>
                    {{ ons }}
                  </h3>
                </b-card-text>
              </b-card>
            </b-col>
            <b-col>
              <b-card border-variant="dark" header="دلار" align="center">
                <template #header>
                  <div style="text-align: center">
                    <p style="color: black">دلار</p>
                  </div>
                </template>
                <b-card-text>
                  <h3>{{ dollar }}</h3>
                </b-card-text>
              </b-card>
            </b-col>
          </b-row>

      
        </b-col>

        <b-col cols="1"></b-col>
      </b-row>

      <br />
    </div>

    <!-- <img
      class="mt-0 mb-0 pt-0 pb-0"
      src="@/assets/background1.jpg"
      alt="طلاگرام"
    /> -->

    <!-- <b-row> 
        <h1> قیمت رسمی طلا و مسکوکات بانکی </h1>
            <b-row><h2> تاریخ امروز </h2> </b-row>
    </b-row> -->
  </div>
</template>

<script>
import axios from "axios";
import config from "@/config";

export default {
  data() {
    return {
      list: [],
      timer: "",

      url1: `${config.paseUrl}` + "api/v1/CurrentPrice/GetTalagram",

      //Date
      today: 0,
      time: "",

      //nerhkha
      dollar: 0,
      ons: 0,
      sekePrice: 0,
      mesghalPrice: 0,
      sekeGhadimPrice: 0,
      sekeRiyal: 0,
      geramTalaPrice: 0,
      gram24TalaPrice: 0,
      nimPrice: 0,
      robPrice: 0,
      sekeGeramiPrice: 0,
    };
  },

  methods: {
    numberWithCommas(x) {
      return x.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
    },
  },

  created() {
    // const d = new Date();
    this.time = new Date().toLocaleTimeString();

    // setInterval(function () {
    //   window.location.reload();
    // }, 20000);
  },

  async mounted() {
    //Date
    this.today = new Date().toLocaleDateString("fa-IR");

    await axios
      .get(`http://localhost:8080/api/v1/CurrentPrice/GetTalagram`, {})

      // await axios
      //   .get(this.url1, {

      //   })
      .then((response) => {
        this.dollar = this.numberWithCommas(response.data.Data.usdPrice);
        this.ons = response.data.Data.onsPrice.toLocaleString();
        this.silver = response.data.Data.silverPrice.toLocaleString();
        this.geramTalaPrice =
          response.data.Data.geramTalaPrice.toLocaleString();
        this.gram24TalaPrice =
          response.data.Data.gram24TalaPrice.toLocaleString();
        this.nimPrice = this.numberWithCommas(response.data.Data.nimPrice);
        this.robPrice = this.numberWithCommas(response.data.Data.robPrice);
        this.sekeGeramiPrice = this.numberWithCommas(
          response.data.Data.sekeGeramiPrice
        );

        this.sekeRiyal = response.data.Data.sekeRiyal;
        this.mesghalRiyal = response.data.Data.mesghalRiyal.toLocaleString();
      })
      .catch((e) => {
        this.errors.push(e);
      });
  },
};
</script>

<style scoped lang="scss">
.d {
  width: 100%;
  height: 100%;
  background-image: url("~@/assets/82.jpg");

  // background-color: #d0ceb5;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
.background {
  height: 100%;
  width: 100%;
}
.up {
  height: 13%;
  background-color: #43413f;
}
.down {
  height: 87%;
  margin-top: 5%;
  //background-image: url("~@/assets/background3.jpg");
}

h1,
h2,
h3,
h4,
h5 {
  color: black;
}

.cont {
  height: 100%;
  width: 100%;
}

.hcolor {
  color: #d0ceb5 !important;
}
.background {
  background-image: url("~@/assets/black.jpg");
  height: 100%;
  width: 100%;
}

.pricediv {
  background-image: url("~@/assets/price.png");
  background-color: #07075c;
  height: 100%;
  width: 85%;
}

.card-header {
  background-color: #dcc588;
}
</style>