<template>
  <div class="provenTrackWrapper">
    <v-row class="mt-12">
      <v-col md="6" cols="12" class="order-last order-md-first">
        <div class="provenTrackContainer">
          <h3 class="provenTrackHeadTitle">
            KWIKmotion™ has a proven track record
          </h3>
          <h4>
            Our system is one of the most reliable, feature-rich Online Video
            solutions available.
          </h4>
          <BaseMainButton text="feature list" />
        </div>
      </v-col>
      <v-col md="6" cols="12" class="d-flex align-center">
        <img
          class="img-holder"
          src="~/assets/imgs/proven-track-record-section/KM.png"
          alt="devices"
        />
      </v-col>
    </v-row>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({});
</script>

<style scoped lang="scss">
.provenTrackWrapper {
  margin: 150px 120px;
  .provenTrackContainer {
    padding-top: 5.9375rem;
    padding-right: 7.25rem;
    h3 {
      color: #333333;
      font-size: 45px;
      line-height: 60px;
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
  .provenTrackWrapper .provenTrackContainer {
    padding-right: 6rem;
  }
}
@media (max-width: 960px) {
  .provenTrackWrapper .provenTrackContainer {
    padding-top: 0;
    padding-right: 0;
    text-align: center;
  }
}
</style>
