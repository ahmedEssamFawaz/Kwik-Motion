<template>
  <div class="kwikFeaturesWrapper">
    <h2 class="featuresHeadTitle">
      Content Creators need Professional Video tools
    </h2>
    <v-row justify="center" no-gutters>
      <v-col
        v-for="(feature, index) in features"
        :key="index"
        md="2"
        sm="4"
        cols="12"
      >
        <v-card class="mx-auto my-12 mainCard" max-width="254" height="235">
          <v-img
            contain
            height="85"
            width="85"
            class="mx-auto"
            :src="
              require(`../../assets/imgs/kwik-features-section/${feature.img}.png`)
            "
          ></v-img>

          <h3 class="cardsTitle">{{ feature.text }}</h3>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  data(): {
    features: {
      text: string;
      img: string;
    }[];
  } {
    return {
      features: [
        {
          text: "Powerful live and VOD capability, from anywhere to everywhere.",
          img: "Group-793",
        },
        {
          text: "Real-time restreaming and syndication to social media.",
          img: "Group-813",
        },
        {
          text: "Cloud based transcoding, packaging and playback.",
          img: "Group-795",
        },
        {
          text: "Flexible Monetisation features.",
          img: "Group-796",
        },
        {
          text: "High quality multi-format streams.",
          img: "Group-816",
        },
      ],
    };
  },
});
</script>

<style scoped lang="scss">
.kwikFeaturesWrapper {
  margin: 150px 0;
  background-color: #F7FFFF;
  .featuresHeadTitle {
    font-size: 45px;
    color: #333;
    text-align: center;
  }
  .mainCard {
    box-shadow: 0px 0px 10px #0000001a;
    padding: 29px 9px;

    .cardsTitle {
      font-size: 20px;
      text-align: center;
      color: #333;
    }
  }
}
@media (max-width: 1199px) {
  .kwikFeaturesWrapper .mainCard .cardsTitle {
    padding-top: 10px;
    font-size: 16px;
  }
}
@media (max-width: 600px) {
  .kwikFeaturesWrapper .mainCard {
    margin-block: 0 !important;
    margin-top: 20px !important;
  }
}
@media (max-width: 960px) {
  .kwikFeaturesWrapper .featuresHeadTitle{
  font-size: 30px;
}
}
</style>
