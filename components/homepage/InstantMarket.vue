<template>
  <div class="instantMarketWrapper">
    <v-row justify="center">
      <v-col md="4" cols="12">
        <div class="img-holder">
          <img
            :src="
              require('@/assets/imgs/instant-market-section/Mask-Group-45.png')
            "
            alt="imgName"
          />
          <h2 class="leftContent">
            <span>ADVANCED CAPABILITY ON A SINGLE PLAYER</span>
          </h2>
        </div>
      </v-col>
      <v-col md="8" cols="12">
        <div class="instantMarketDescWrapper">
          <div class="instantMarketHeadTitle">Instantly to market</div>
          <v-list dense three-line flat disabled color="transparent">
            <v-list-item-group>
              <v-list-item v-for="service in services" :key="service.id">
                <v-list-item-icon class="d-flex">
                  <v-img
                    contain
                    height="11"
                    width="11"
                    class="mx-auto"
                    :src="
                      require('../../assets/imgs/instant-market-section/Rectangle-355.png')
                    "
                  ></v-img>
                </v-list-item-icon>
                <v-list-item-content>
                  <span class="serviceListTitles">{{ service.name }}</span>
                  <p>{{ service.desc }}</p>
                </v-list-item-content>
              </v-list-item>
            </v-list-item-group>
          </v-list>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import jsonData from "../../static/data/InstantMarket.json";

export default Vue.extend({
  data(): {
    services: {
      id: number;
      name: string;
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

.instantMarketWrapper {
  margin: 250px 0 0 0;
  .img-holder {
    width: 853px;
    position: relative;
    z-index: 2;
    img {
      max-width: 100%;
    }
    .leftContent {
      background: url("~/assets/imgs/instant-market-section/Group-817.png");
      line-height: 1.4;
      padding: 20px 122px 121px 65px;
      width: 400px;
      margin: 20px auto;
      background-repeat: no-repeat;
      position: absolute;
      top: 56%;
      right: 27%;
      left: 0;

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
  }
  .instantMarketDescWrapper {
  position: relative;
  background-color: #ffd100;
  padding: 37px 35px 20px 57px;
  min-height: 30.9375rem;
  background-image: url("@/assets/imgs/instant-market-section/Mask-Group-37.png");
  background-position: 107% 104%;
  .serviceListTitles {
  font-size: 20px;
  color: #333;
  font-weight: bold;
}
  .instantMarketHeadTitle {
    font-size: 45px;
    color: #333;
    line-height: 60px;
    font-weight: bold;
    text-align: left;
    margin-bottom: 15px;
  }
}
}

</style>
