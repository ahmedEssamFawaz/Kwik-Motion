<template>
  <div class="kwikCustomerTypeWrapper">
    <h2 class="customerTypeHeadTitle mb-10">Are you a typical KWIKmotion™ customer?</h2>
    <v-row no-gutters>
      <v-col
        v-for="service in services"
        :key="service.id"
        md="3"
        cols="12"
      >
        <v-card class="mx-auto mt-7 customerTypeCard" max-width="319" height="295" :to="service.link" >
                <v-img
                class="img-container"
                :src="
                    require(`../../assets/imgs/kwik-motion-customer-type-section/${service.image}.png`)
                  "
                  max-height="195"
                ></v-img>

          <h3 class="customerTypeCardTitle">{{ service.name }}</h3>

          
        </v-card>
            </v-col>
    </v-row>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import jsonData from "../../static/data/KwikmotionCustomerType.json";

export default Vue.extend({
  data(): {
    services: {
      id: number;
      name: string;
      image: string;
      link: string;
    }[];
  } {
    return {
      services: jsonData.services,
    };
  },
});
</script>

<style  lang="scss">
.img-container > .v-image__image--cover{
background-size: auto;
}
.kwikCustomerTypeWrapper {
  background-color: #F7FFFF;
  margin-top: 100px;
  .customerTypeHeadTitle {
    font-size: 45px;
    color: #333;
    text-align: center;
  }
  .customerTypeCard {
    box-shadow: 0px 0px 10px #0000001a !important;

    .customerTypeCardTitle {
      font-size: 20px;
      text-align: center;
      color: #333;
      margin-top: 32px;
    }
  }
}
@media (max-width: 1330px) {
    .kwikCustomerTypeWrapper .customerTypeCard .customerTypeCardTitle {
    font-size: 18px;
  }
}
@media (max-width: 1199px) {
  .kwikCustomerTypeWrapper .customerTypeCard .customerTypeCardTitle {
    padding-top: 10px;
    font-size: 16px;
  }
}
@media (max-width: 960px) {
    .kwikCustomerTypeWrapper .customerTypeHeadTitle{
      font-size: 28px;
      line-height: 40px;
    }
  }
@media (max-width: 600px) {
  .kwikCustomerTypeWrapper .customerTypeCard {
    margin-block: 0 !important;
    margin-top: 20px !important;
  }
}
</style>
