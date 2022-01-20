<template>
  <div class="d">
      <br />
      <br />
    

      <b-row dir="rtl">
        <b-col cols="2"> </b-col>

        <b-col class="mt-2 " cols="8">
          <b-row class="mt-2 m">
            <b-col align="center">
              <v-card elevation="15">
                <v-alert outlined color="black ">
                  <h5 class="fcolor">
                    <b> قیمت رسمی طلا و مسکوکات بانکی امروز : {{ today }} </b>
                  </h5>
                </v-alert>
              </v-card>
            </b-col>
          </b-row>

          <b-row>
            <div class="img1"></div>

            <b-col>
              <v-card elevation="15">
                <v-alert outlined color="black">
                  <h5 class="hcolor" style="font-size:16px" align="center">
                    <b> طلا 18 عیار </b>
                  </h5>
                </v-alert>
              </v-card>
            </b-col>

            <b-col>
              <v-card elevation="15">
                <v-alert outlined color="black ">
                  <h5 align="center">
                    <b> {{ geramTalaPrice }} </b>
                  </h5>
                </v-alert>
              </v-card>
            </b-col>
          </b-row>

          <br />

          <b-row>
            <div class="img1"></div>

            <b-col>
              <v-card elevation="15">
                <v-alert outlined color="black ">
                  <h5 class="hcolor" style="font-size:16px" align="center">
                    <b> طلا 24 عیار </b>
                  </h5>
                </v-alert>
              </v-card>
            </b-col>

            <b-col>
              <v-card elevation="15">
                <v-alert outlined color="black ">
                  <h5 align="center">
                    <b> {{ gram24TalaPrice }} </b>
                  </h5>
                </v-alert>
              </v-card>
            </b-col>
          </b-row>

          <br />

          <b-row>
            <div class="img2"></div>

            <b-col>
              <v-card elevation="15">
                <v-alert outlined color="black ">
                  <h5 class="hcolor" align="center">
                    <b> تمام سکه </b>
                  </h5>
                </v-alert>
              </v-card>
            </b-col>

            <b-col>
              <v-card elevation="15">
                <v-alert outlined color="black ">
                  <h5 align="center">
                    <b> {{ sekeGeramiPrice }} </b>
                  </h5>
                </v-alert>
              </v-card>
            </b-col>
          </b-row>

          <br />

          <b-row>
            <div class="nim"></div>

            <b-col>
              <v-card elevation="15">
                <v-alert outlined color="black ">
                  <h5 class="hcolor" align="center">
                    <b> نیم سکه </b>
                  </h5>
                </v-alert>
              </v-card>
            </b-col>

            <b-col>
              <v-card elevation="15">
                <v-alert outlined color="black ">
                  <h5 align="center">
                    <b> {{ nimPrice }} </b>
                  </h5>
                </v-alert>
              </v-card>
            </b-col>
          </b-row>

          <br />

          <b-row>
            <div class="rob"></div>

            <b-col>
              <v-card elevation="15">
                <v-alert outlined color="black ">
                  <h5 class="hcolor" align="center">
                    <b> ربع سکه </b>
                  </h5>
                </v-alert>
              </v-card>
            </b-col>

            <b-col>
              <v-card elevation="15">
                <v-alert outlined color="black ">
                  <h5 align="center">
                    <b> {{ robPrice }} </b>
                  </h5>
                </v-alert>
              </v-card>
            </b-col>
          </b-row>

          <br />
          <b-row>
            <b-col align="center">
              <v-card elevation="15">
                <v-alert outlined color="black ">
                  <h5 class="fcolor">
                    <b> شیراز - فرهنگ شهر - کوچه بانک ملت 0987654330 </b>
                  </h5>
                </v-alert>
              </v-card>
            </b-col>
          </b-row>
        </b-col>

        <b-col cols="2"> </b-col>
      </b-row>


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
        this.dollar = response.data.Data.usdPrice;
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
        this.talaAyarPriceOpen = response.data.Data.talaAyarPriceOpen;

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
  background-image: url("~@/assets/background2.jpg");
   background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

.img1 {
  background-image: url("~@/assets/50.png") ;
  height: 4em;
  width: 4em;
  margin-right: 1rem;
 // background-color: red;
}

.img2 {
  background-image: url("~@/assets/51.png");
  height: 4rem;
  width: 4rem;
  margin-right: 1rem;
}

.hcolor {
  color: #bea44d;
}

.col10 {
  background-color: #fbf2af;
}
.rob {
  background-image: url("~@/assets/51.png");
  height: 4rem;
  width: 4rem;
  margin-right: 1rem;
}

.nim {
  background-image: url("~@/assets/51.png");
  height: 4rem;
  width: 4rem;
  margin-right: 1rem;
}

.tamam {
  background-image: url("~@/assets/51.png");
  height: 4rem;
  width: 4rem;
  margin-right: 1rem;
}
</style>