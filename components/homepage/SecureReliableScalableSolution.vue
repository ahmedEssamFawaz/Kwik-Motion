<template>
  <div class="solutionsWrapper">
    <v-row justify="center" no-gutters>
      <v-col md="6" cols="12" class="order-last order-md-first">
        <h3 class="solutionsHeadTitle">
          We make sure your solution is secure, reliable, scalable
        </h3>
        <v-list dense two-line flat disabled>
          <v-list-item-group color="primary">
            <v-list-item v-for="solution in solutions" :key="solution.id">
              <v-list-item-icon>
                <v-img
                  contain
                  height="34"
                  width="42"
                  class="mx-auto"
                  :src="
                    require(`../../assets/imgs/secure-reliable-scalable-solution-section/${solution.icon}.png`)
                  "
                ></v-img>
              </v-list-item-icon>
              <v-list-item-content>
                <span class="solutionTitles">{{ solution.name }}</span>
              </v-list-item-content>
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-col>
      <v-col md="6" cols="12">
        <img
          class="mx-auto img-holder"
          src="~/assets/imgs/secure-reliable-scalable-solution-section/Mask-Group-40.png"
          alt="laptop"
        />
      </v-col>
    </v-row>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import jsonData from "../../static/data/SecureReliableScalableSolution.json";

export default Vue.extend({
  data(): {
    solutions: {
      id: number;
      name: string;
      icon: string;
    }[];
  } {
    return {
      solutions: jsonData.solutions,
    };
  },
});
</script>

<style scoped lang="scss">
.solutionsWrapper {
  margin: 150px 120px;
  .solutionsHeadTitle {
    font-size: 45px;
    color: #333;
    font-weight: bold;
  }
  .solutionTitles{
    font-size: 20px;
    color: #333;
    font-weight: 600;
  }
  .img-holder {
  max-width: 100%;
  margin-top:181px;
}

}

@media (max-width: 960px) {
  .solutionsWrapper{
    margin: 150px 31px;
    
    .img-holder{
      margin-top:50px;
  
    }
  } 
}
</style>
