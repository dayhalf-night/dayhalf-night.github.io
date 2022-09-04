<script lang="ts">
  
import { NCard, NSpace } from 'naive-ui';
import anchor from './components/anchor.vue';
import calculate from './components/calculate.vue';
import homePage from './components/homePage.vue';
import netanalysis from './components/netanalysis.vue';
import textanalysis from './components/textanalysis.vue';
  export default {
    components:{
      anchor,
      homePage,
      NCard,
      calculate,
      NSpace,
      textanalysis,
      netanalysis
    }
  }
</script>
  
<template>
  <n-space vertical>
    <n-card id="homepage">
      <div style="width:1000px;height: 500px;margin: 0px;text-align: center;">
        <homePage />
      </div>
    </n-card>
    <n-card id="calculate">
      <div style="width:1000px;height: 500px;margin: 0px;">
        <calculate />
      </div>
    </n-card>
    <n-card id="textAnalysis" title="文本分析">
      <textanalysis />
    </n-card>
    <n-card id="netAnalysis" title="传播网络">
      <netanalysis />
    </n-card>
  </n-space>
  <div style="float:left;width:200px;">
    <anchor />
  </div>
  

</template>

<style scoped> 
  .n-card{
    height: 740px;
  }
</style>
  