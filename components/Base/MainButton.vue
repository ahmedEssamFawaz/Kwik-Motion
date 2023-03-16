<template>
  <v-btn elevation="0" color="#ffd100" class="mainButton text-capitalize " large
    >{{text}}</v-btn
  >
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
    props:{
            text:{
                type:String,
                required:false
            }
        }
});
</script>

<style scoped>
.mainButton{
    color: #333;
    font-size: 14px;
    padding: 12px 41px 10px 41px;
}
</style>
