<template>
  <div class="contactUsWrapper">
    <v-row no-gutters>
      <v-col md="12" cols="12">
        <div class="contactUsContainer">
          <v-row no-gutters>
            <v-col cols="12">
              <div class="contactUsBox">
                <div class="text-center">
                  <p>
                    Want more information or a demonstration of why KWIKmotion™
                    could be the single solution video platform for you?
                  </p>
                  <BaseMainButton text="contact us" />
                </div>
              </div>
              <div class="imgHolderWrapper">
                <img
                  class="img-holder"
                  :src="
                    require(`../../assets/imgs/contact-us-section/dragon-contact.png`)
                  "
                  alt="dragon"
                />
              </div>
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
.contactUsWrapper {
  margin: 364px 0 0 0;
  .contactUsContainer {
    background-color: #ffd100;
    height: 215px;
    background-image: url("@/assets/imgs/kwik-functionality-section/Group-799.png");
    background-position: 1px -4px;
    position: relative;
    .contactUsBox {
      height: 277px;
      width: 531px;
      background-color: #fff;
      box-shadow: 0px 0px 10px #0000001a;
      border-radius: 10px;
      margin: 0 auto;
      position: absolute;
      bottom: 36%;
      left: 0;
      right: 0;
      p {
        margin-bottom: 0;
        padding: 55px 46.5px;
        font-weight: bold;
        font-size: 20px;
        position: relative;
        z-index: 1;
      }
    }
    .imgHolderWrapper{
    position: absolute;
    left: 53%;
    bottom: 2%;
    .img-holder{
        max-width: 100%;
    }
}
  }
}


@media (max-width: 1251px) {
    .contactUsWrapper .contactUsContainer .imgHolderWrapper{
    // display: none;

}
}
@media (max-width: 627px) {
    .contactUsWrapper .contactUsContainer .contactUsBox{
    width: 373px;
  p{
    font-size: 16px;
  }
}

}

</style>
