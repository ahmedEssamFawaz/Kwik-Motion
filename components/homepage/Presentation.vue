<template>
  <v-row no-gutters>
    <v-col md="8" cols="12">
      <div class="presentationDesc">
        <v-row no-gutters>
          <v-col md="6" cols="12">
            <div class="presentationTitle">
              KWIKmotion™ is a monster <br />Online Video Solution
            </div>
            <div class="presentationSubTitle mt-5">
              This is an OVP solution that goes much further than you imagine
            </div>
            <div class="presentationSubTitle mt-5">
              KWIKmotion™ has a pedigree built over ten years of innovation,
              reliability and robust functionality for a diverse customer group.
            </div>
            <div class="presentationSubTitle mt-5">
              It’s so good, it’s frightening.
            </div>
          </v-col>
          <v-col md="6" cols="12">
            <div class="presentationMainImg"></div>
          </v-col>
        </v-row>
      </div>
    </v-col>
    <v-col md="4" cols="12">
      <h2 class="rightContent">
        <span>DELIVER STUNNING FEATURE-RICH VIDEO TO ANY DEVICE</span>
      </h2>
    </v-col>
  </v-row>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({});
</script>

<style scoped lang="scss">
.presentationDesc {
  background-color: #ffd100;
  padding: 57px 35px 20px 250px;
  min-height: 30.9375rem;
  background-image: url("@/assets/imgs/presentation-section/Group-789.png");
  background-position: -99px -4px;
  position: relative;
  .presentationTitle {
    font-size: 45px;
    color: #333;
    line-height: 60px;
    font-weight: bold;
    text-align: left;
    margin-bottom: 15px;
  }
  .presentationSubTitle {
    font-size: 20px;
    font-weight: bold;
  }
}
.presentationMainImg {
  background-image: url("@/assets/imgs/presentation-section/dragon-new.png");
  height: 100%;
  background-size: contain;
  position: absolute;
  width: 100%;
  top: 15%;
  left: 56%;
}
.rightContent {
  background: url("~/assets/imgs/presentation-section/Group-791.png");
  line-height: 1.4;
  padding: 20px 107px 121px 50px;
  width: 400px;
  margin: 20px auto;
  background-repeat: no-repeat;
  position: relative;
  span {
    font-size: 20px;
    color: #333;
    text-transform: uppercase;
    font-weight: bold;
    position: relative;
    right: 29px;
    top: 25px;
  }
}
@media (max-width: 1565px) {
  .presentationMainImg {
    width: 83%;
    top: 28%;
    left: 49%;
  }
  .presentationDesc {
    padding: 57px 0px 20px 70px;
  }
  .rightContent {
    padding: 20px 0px 121px 50px;
    max-width: 263px;
  }
}
@media (max-width: 1229px) {
  .presentationMainImg {
    width: 83%;
    top: 28%;
    left: 49%;
  }
  .presentationDesc {
    .presentationTitle {
      font-size: 28px;
      line-height: 40px;
    }
    .presentationSubTitle {
      font-size: 16px;
    }
  }
}
@media (max-width: 959px) {
  .presentationDesc .presentationSubTitle {
    position: relative;
    z-index: 2;
  }
  .presentationMainImg {
    left: 32%;
    width: 70%;
    top: 41%;
  }
}
@media (max-width: 769px) {
  .presentationMainImg {
    left: 35%;
    width: 64%;
    top: 54%;
  }
}
@media (max-width: 650px) {
  .presentationMainImg {
    left: 32%;
    top: 70%;
  }
}
@media (max-width: 524px) {
  .presentationMainImg {
    top: 79%;
  }
}
@media (max-width: 354px) {
  .presentationMainImg {
    top: 89%;
  }
}
</style>
