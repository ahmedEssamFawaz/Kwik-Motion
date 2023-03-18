<template>
    <div class="containerWrapper" :style="{backgroundColor: '#'+bgColor}">
      <v-row class="mt-12" no-gutters>
        <v-col md="6" cols="12" class="order-last order-md-first">
          <div class="holder">
            <h3>
              {{headTitle}}
            </h3>
            <h4 class="mt-7">
             {{subHeadTitle}}
            </h4>
            <BaseMainButton v-if="btnText" :text="btnText" />
          </div>
        </v-col>
        <v-col md="6" cols="12" class="d-flex align-center justify-center">
          <img
            class="img-holder"
            :src="
              require(`../../assets/imgs/${destinationFolderImg}/${imgName}`)
            "
            :alt="imgName"
          />
        </v-col>
      </v-row>
    </div>
  </template>
  
  <script lang="ts">
  import { Vue, Component, Prop } from "vue-property-decorator";
  
  @Component
  export default class ImageTextCard extends Vue {
    @Prop({ type: String, required: true }) headTitle!: string;
    @Prop({ type: String, required: false }) subHeadTitle?: string;
    @Prop({ type: String, required: false }) btnText?: string;
    @Prop({ type: String, required: true }) destinationFolderImg!: string;
    @Prop({ type: String, required: true }) imgName!: string;
    @Prop({ type: String, required: false , default: 'fff' }) bgColor!: string;

  }
  </script>
  
  <style scoped lang="scss">
  .containerWrapper {
    padding: 20px 120px;
    .holder {
      padding-top: 5.9375rem;
      padding-right: 7.25rem;
      h3 {
        color: #333333;
        font-size: 45px;
        line-height: 60px;
      }
      h4{
        font-size: 20px;
      }
      > * {
        margin-bottom: 15px;
        &:last-child {
          margin-bottom: 0;
        }
      }
    }
  
    .img-holder {
      max-width: 100%;
    }
  }
  @media (max-width: 1400px) {
    .containerWrapper .holder {
      padding-right: 6rem;
    }
  }
  @media (max-width: 960px) {
    .containerWrapper {
      padding-inline: 0;
      .holder {
        padding-top: 0;
        padding-right: 0;
        text-align: center;
        h3{
          font-size: 28px;
          line-height: 40px;
        }
        h4{
          font-size: 16px;
        }
      }
    }
  }
  </style>
  