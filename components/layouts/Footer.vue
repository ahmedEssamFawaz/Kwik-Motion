<template>
  <v-footer dark padless min-height="403" color="#333333">
    <v-card flat tile height="100%" class="footerContainer">
      <v-row no-gutters>
        <v-col md="2" cols="12">
          <v-card-text>
            <!-- Logo section -->
            <img
              src="~/assets/imgs/footer-logo/Group 864@2x.png"
              alt="footer Logo"
              height="70"
            />
          </v-card-text>
        </v-col>
        <v-col md="4" cols="12">
          <div class="d-flex justify-space-between flex-wrap">
            <div class="d-flex flex-column align-start">
              <v-card-title class="pb-0 mainColor">Products</v-card-title>
              <v-btn
                v-for="link in productsLinks"
                :key="link.text"
                color="white"
                text
                :ripple="false"
                rounded
                class="my-1"
              >
                {{ link.text }}
              </v-btn>
            </div>
            <div class="d-flex flex-column align-start">
              <v-card-title class="pb-0 mainColor">Corporate</v-card-title>
              <v-btn
                v-for="link in corporateLinks"
                :key="link.text"
                color="white"
                text
                rounded
                :ripple="false"
                class="my-1"
              >
                {{ link.text }}
              </v-btn>
            </div>
            <div class="d-flex flex-column align-start">
              <v-card-title class="pb-0 mainColor">Blog</v-card-title>
              <v-btn
                v-for="link in blogLinks"
                :key="link.text"
                :color="link.color ? link.color : 'white'"
                text
                :ripple="false"
                rounded
                class="my-1"
              >
                {{ link.text }}
              </v-btn>
            </div>
          </div>
        </v-col>
        <v-col md="6" cols="12">
          <div class="subscribeContainer">
            <label for="newsLetter"  class="subscribeLabel white--text">NewsLetter</label >
            <input
            id="newsLetter" name="newsLetter"
              placeholder="Email Address"
              class="newsLetterInput"
              type="text"
            />
            <v-btn class="subscribeButton my-1 ml-3 text-capitalize" large>
              Subscribe
            </v-btn>
            <div>
              <v-btn class="loginButton my-1 ml-3 text-capitalize" large text>
                Login
              </v-btn>
              <BaseMainButton text="Request Demo"/>

            </div>
          </div>
        </v-col>
      </v-row>

      <v-row justify="center" class="mt-15" no-gutters>
        <v-col cols="8">
          <div class="d-flex justify-space-between privacyLinksContainer">
            <div class="servicesLinks">
              <span>
                <v-btn text>
                  Terms of service
                </v-btn>
                |
                <v-btn class="pl-0" text>
                Privacy Policy
                </v-btn>
                |
                <v-btn text class="pl-0">
                  Cookies
                </v-btn>
              </span>
  
            </div>
            <div class="tradeMarkText">
              <p>&copy; 2023 - All Rights Reserved &copy;KWIKmotion&trade;</p>
  
            </div>

          </div>
        </v-col>

      </v-row>
    </v-card>
  </v-footer>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  data(): {
    productsLinks: {
      text: string;
      link: string;
    }[];
    corporateLinks: {
      text: string;
      link: string;
    }[];
    blogLinks: {
      text: string;
      link: string;
      color?: string;
    }[];
  } {
    return {
      productsLinks: [
        {
          text: "KWIKprime",
          link: "/",
        },
        {
          text: "KWIKplayer",
          link: "/",
        },
        {
          text: "KWIKintelligence",
          link: "/",
        },
        {
          text: "KWIKeditor",
          link: "/",
        },
        {
          text: "KWIKanalytics",
          link: "/",
        },
      ],
      corporateLinks: [
        {
          text: "About",
          link: "/",
        },
        {
          text: "Partners",
          link: "/",
        },
        {
          text: "Success Stories",
          link: "/",
        },
      ],
      blogLinks: [
        {
          text: "Contact Us",
          link: "/",
          color: "#FFD100",
        },
      ],
    };
  },
});
</script>

<style scoped lang="scss">
.footerContainer {
  padding: 76px 15px 30px 15px;
  width: 100vw;
}
.mainColor {
  color: #ffd100;
}
.subscribeContainer {
  padding-right: 21px;
  padding-left: 42px;
  padding-bottom: 10px;
  padding-top: 16px;
  .subscribeLabel {
    font-size: 14px;
    display: block;
  }
  .newsLetterInput {
    border-radius: 3px 3px 3px 3px;
    background-color: #525252;
    border: none;
    width: calc(100% - 450px);
    color: #fff;
    padding: 11px 0 13px 13px;
  }
}
.v-btn.subscribeButton {
  padding: 12px 41px 10px 41px;
  color: #fff;
  border: 1px solid #ffd100;
  border-radius: 3px;
  background-color: #525252;
  font-size: 16px;
  text-align: center;
}
.loginButton {
  color: #fff;
  padding-right: 14px;
  padding-top: 11px;
}
.servicesLinks .v-btn{
  font-size: 12px;
    text-transform: capitalize;
    padding-right: 0;
}
.tradeMarkText{
  font-size: 12px;
  align-self: center;
  p{
    margin: 0;
  }
}
@media (max-width: 1400px){
  .subscribeContainer{
    .newsLetterInput {
        width: calc(100% - 200px);
    }

  }
  
}
@media (max-width: 960px){
  .subscribeContainer{
padding-left: 14px; 

  }
  
}

@media (max-width: 881px){
  .privacyLinksContainer{
    display: block !important;
    text-align: center;
  }
  
}
</style>
