<template>
  <div class="kwikFunctionalityWrapper">
    <v-row class="my-12">
      <v-col md="12" cols="12">
        <div class="kwikFunctionalityContainer">
          <v-row>
            <v-col md="6" sm="4" cols="12">
              <div class="kwikFunctionalityMainImg" />
            </v-col>
            <v-col md="6" sm="8" cols="12">
              <h2 class="commentImg">
                <span
                  >AND THE ICING ON THE CAKE? THE KWIKmotion™ EXTRA
                  FUNCTIONALITY</span
                >
              </h2>
            </v-col>
          </v-row>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({});
</script>

<style scoped lang="scss">
.kwikFunctionalityWrapper {
  margin: 230px 0 0 0;
}
.kwikFunctionalityContainer {
  background-color: #ffd100;
  height: 188px;
  background-image: url("@/assets/imgs/kwik-functionality-section/Group-799.png");
  background-position: 1px -4px;
  .kwikFunctionalityMainImg {
    background-image: url("@/assets/imgs/kwik-functionality-section/Mask-Group-46.png");
    height: 509px;
    position: relative;
    background-size: contain;
    bottom: 42%;
    left: 10%;
    z-index: 1;
  }
  .commentImg {
    background: url("@/assets/imgs/kwik-functionality-section/Group-663.png");
    line-height: 1.4;
    padding: 20px 50px 135px 50px;
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
      top: 60px;
    }
  }
}

@media (max-width: 960px) {
  .kwikFunctionalityContainer .kwikFunctionalityMainImg {
    height: 270px;

    bottom: 15%;
  }
}
@media (max-width: 600px) {
  .kwikFunctionalityContainer .kwikFunctionalityMainImg {
    display: none;
  }
}
</style>
