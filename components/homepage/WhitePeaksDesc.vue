<template>
  <div class="whitePeaksDescWrapper">
    <v-row justify="center">
      <v-col md="6" cols="12">
        <div class="whitePeaksDescContainer">
          <v-img
            contain
            height="109"
            width="227"
            :src="
              require(`../../assets/imgs/white-peaks-desc-section/wps-logotype_gradient2.png`)
            "
          ></v-img>
          <div class="whitePeaksHeadTitle">Who is White Peaks Solutions?</div>

          <v-list dense two-line flat disabled color="transparent">
            <v-list-item-group>
              <v-list-item v-for="service in services" :key="service.id">
                <v-list-item-icon class="d-flex">
                  <v-img
                    contain
                    height="11"
                    width="11"
                    class="mx-auto"
                    :src="
                      require('../../assets/imgs/white-peaks-desc-section/Arrow-Bullet.png')
                    "
                  ></v-img>
                </v-list-item-icon>
                <v-list-item-content>
                  <p class="serviceDesc">{{ service.desc }}</p>
                </v-list-item-content>
              </v-list-item>
            </v-list-item-group>
          </v-list>
          <div class="whitePeaksBtnHolder">
            <v-btn
              elevation="0"
              color="#00AEF6"
              class="whitePeaksBtn text-capitalize"
              large
              >Visit our website</v-btn
            >
          </div>
        </div>
      </v-col>
      <v-col md="6" cols="12">
        <div class="img-wrapper">
          <img
            class="img-holder"
            :src="
              require(`../../assets/imgs/white-peaks-desc-section/Image-1.png`)
            "
            alt="laptop"
          />
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import jsonData from "../../static/data/whitePeaksServices.json";

export default Vue.extend({
  data(): {
    services: {
      id: number;
      desc: string;
    }[];
  } {
    return {
      services: jsonData.services,
    };
  },
});
</script>

<style scoped lang="scss">
.whitePeaksDescWrapper {
  margin: 0 0 0 0;
  background-image: url("@/assets/imgs/white-peaks-desc-section/Group-788.png");
  background-size: cover;

  .whitePeaksDescContainer {
    position: relative;
    padding: 37px 35px 20px 57px;
    min-height: 30.9375rem;

    .serviceListTitles {
      font-size: 20px;
      color: #333;
      font-weight: bold;
    }
    .whitePeaksHeadTitle {
      font-size: 35px;
      color: #333;
      line-height: 60px;
      font-weight: bold;
      text-align: left;
      margin-top: 1.8125rem;
    }
    .serviceDesc {
      font-size: 16px;
    }
  }
  .img-wrapper {
    padding-top: 120px;
    .img-holder {
      max-width: 100%;
    }
  }
  .whitePeaksBtnHolder {
    padding-left: 70px;
    .whitePeaksBtn {
      color: #fff;
      font-weight: 500;
    }
  }
}
@media (max-width: 960px) {
  .whitePeaksDescWrapper .img-wrapper {
    padding-top: 0;
    text-align: center;
  }
}
</style>
