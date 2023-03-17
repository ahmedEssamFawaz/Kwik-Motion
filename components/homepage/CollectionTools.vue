<template>
  <div class="collectionToolsWrapper">
    <h2 class="collectionToolsHeadTitle">
      Instantly to market with our collection of KWIKmotion™ tools
    </h2>
    <v-row justify="center">
      <v-col v-for="tool in tools" :key="tool.id" md="2" sm="4" cols="12">
        <v-card class="mx-auto my-12 mainCard" max-width="254" height="235">
          <v-card-text class="px-0 mb-5">
            <v-img
              contain
              height="52"
              width="170"
              class="mx-auto"
              :src="
                require(`../../assets/imgs/collection-tools-section/${tool.image}.png`)
              "
            ></v-img>
          </v-card-text>
          <v-card-text class="cardsTitleHolder">
            <h3 class="cardsTitle">{{ tool.name }}</h3>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
    <h2 class="collectionToolsHeadTitle">
        Part of the White Peaks Solutions powerful OTT Solution
    </h2>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import jsonData from "../../static/data/tools.json";

export default Vue.extend({
  data(): {
    tools: {
      id: number;
      name: string;
      image: string;
    }[];
  } {
    return {
      tools: jsonData.tools,
    };
  },
});
</script>

<style scoped lang="scss">
.collectionToolsWrapper {
  margin: 150px 0 80px 0;
  .collectionToolsHeadTitle {
    font-size: 45px;
    color: #333;
    text-align: center;
  }
  .mainCard {
    box-shadow: 0px 10px 10px #0000001a;
    padding: 0;
    display: flex;
    flex-direction: column;
    justify-content: end;
    .cardsTitleHolder {
        height: 112px;
      background-color: #ffd100;
      .cardsTitle {
        font-size: 16px;
        text-align: center;
        color: #333;
        font-weight: 500;
      }
    }
  }
}
@media (max-width: 1199px) {
  .collectionToolsWrapper .mainCard .cardsTitle {
    padding-top: 10px;
    font-size: 16px;
  }
}
@media (max-width: 600px) {
  .collectionToolsWrapper .mainCard {
    margin-block: 0 !important;
    margin-top: 20px !important;
  }
}
</style>
