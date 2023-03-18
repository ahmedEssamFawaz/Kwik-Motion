<template>
  <v-row class="my-12" no-gutters>
    <v-col md="12" cols="12">
      <div class="fanEngagementWrapper">
        <v-row no-gutters>
          <v-col  md="6"  cols="12">
            <h2 class="commentImg">
              <span
                >BUT WE DO MUCH MORE THAN GET THE ‘RIGHT CONTENT TO THE RIGHT
                FANS’</span
              >
            </h2>
          </v-col>
          <v-col  md="6"  cols="12" class="mainImgHolder">
            <div class="fanEngagementMainImg" />
          </v-col>
        </v-row>
      </div>
    </v-col>
  </v-row>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({});
</script>

<style scoped lang="scss">

.fanEngagementWrapper {
  background-color: #ffd100;
  height: 188px;
  background-image: url("@/assets/imgs/fan-engagement-section/Group-798.png");
  background-position: 100% 12%;
  .mainImgHolder{
  position: relative;
  .fanEngagementMainImg {
    background-image: url("@/assets/imgs/fan-engagement-section/Right-content.png");
  height: 509px;
    position: absolute;
    width: 563px;
    background-size: contain;
    bottom: -23%;
    left: 10%;
    z-index: 1;
  }
}

  .commentImg {
    background: url("@/assets/imgs/fan-engagement-section/Group-797.png");
    line-height: 1.4;
    padding: 20px 50px 121px 50px;
    width: 400px;
    margin: 1px auto;
    background-repeat: no-repeat;
    position: relative;
    z-index: 2;
    span {
      font-size: 20px;
      color: #333;
      text-transform: uppercase;
      font-weight: bold;
      position: relative;
      right: 12px;
      top: 38px;
    }
  }
}
@media (max-width: 1635px){
    .fanEngagementWrapper .mainImgHolder .fanEngagementMainImg {
    height: 370px;
      width: 372px;
    bottom: -8%;
}
}

@media (max-width: 960px){
    .fanEngagementWrapper .mainImgHolder .fanEngagementMainImg {
    display: none;
}
}

</style>
