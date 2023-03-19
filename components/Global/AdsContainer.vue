<template>
  <div class="adsContainerWrapper">
    <v-row class="my-12" no-gutters>
      <v-col md="12" cols="12">
        <div class="adsContainerHolder">
          <v-row no-gutters>
            <v-col md="6" cols="12">
              <div  class="mainImgHolder">
                <div class="adsContainerMainImg" :style="{ backgroundImage: `url(${require(`@/assets/imgs/${destinationFolderImg}/${imgName}`)})` }" />

              </div>
            </v-col>
            <v-col md="6" cols="12">
              <div class="holder">
                <h3>
                  {{ headTitle }}
                </h3>
                <h4>
                  {{ subHeadTitle }}
                </h4>
              </div>
            </v-col>
            <v-col  cols="12">
              <div  class="smImgHolder">
<v-img :src="require(`@/assets/imgs/${destinationFolderImg}/${imgName}`)" height="250" contain/>
              </div>
            </v-col>
          </v-row>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script lang="ts">
import { Vue, Component, Prop } from "vue-property-decorator";

@Component
export default class ImageTextCard extends Vue {
  @Prop({ type: String, required: true }) headTitle!: string;
  @Prop({ type: String, required: true }) subHeadTitle!: string;
  @Prop({ type: String, required: false }) destinationFolderImg!: string;
  @Prop({ type: String, required: false }) imgName!: string;
}
</script>

<style scoped lang="scss">
.adsContainerWrapper {
  margin-top: 10rem;
  .adsContainerHolder {
    background-color: #ffd100;
    height: 314px;
    background-image: url("@/assets/imgs/kwik-functionality-section/Group-799.png");
    background-position: -30px 27px;
    .smImgHolder{
      display: none;
    }
    .holder {
      padding-top: 3.5625rem;
      padding-right: 7.25rem;
      h3 {
        color: #333333;
        font-size: 45px;
        line-height: 60px;
      }
      h4{
        padding-top: 2.5rem;
      }

      > * {
        margin-bottom: 15px;
        &:last-child {
          margin-bottom: 0;
        }
      }
    }
    .mainImgHolder{
        position: relative;
        .adsContainerMainImg {
        height: 509px;
    position: absolute;
    width: 563px;
    background-size: contain;
    top: -14%;
    left: 10%;
    z-index: 1;
    }
    }
 
  }
}

@media (max-width: 1093px) {
    .adsContainerWrapper  .adsContainerHolder .mainImgHolder .adsContainerMainImg {
    width: 470px;
    top: 9%;
  }
}
@media (max-width: 960px) {
    .adsContainerWrapper .adsContainerHolder .holder{
        padding-top: 2rem;
    padding-left: 1.25rem;
    padding-right: 2.25rem;
    }
    .adsContainerWrapper  .adsContainerHolder .mainImgHolder .adsContainerMainImg {
    display: none;
  }
  .adsContainerWrapper .adsContainerHolder .smImgHolder{
    display: block;
  }
}
</style>
