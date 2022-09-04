<script lang="ts">
  import type { AnchorInst } from 'naive-ui'
import { NAnchor, NAnchorLink } from 'naive-ui'
import { defineComponent, ref } from 'vue'
  
  export default defineComponent({
    components:{
      NAnchor,
      NAnchorLink
    },
    setup () {
      const anchorRef = ref<AnchorInst | null>(null)
      const scrollTo = (href: string) => {
        anchorRef.value?.scrollTo(href)
      }
      return {
        anchorRef,
        scrollTo
      }
    }
  })
  </script>
<template>
    <n-anchor
      ref="anchorRef"
      affix
      :trigger-top="24"
      :top="88"
      :bound="24"
      style="z-index: 1"
      type="block"
      :ignore-gap="true"
    >
    <n-anchor-link>
      <n-anchor-link title="首页" href="#homepage" />
      <n-anchor-link title="预测" href="#calculate" />
      <n-anchor-link title="文本分析" href="#textAnalysis" />
      <n-anchor-link title="网络分析" href="#netAnalysis" />
    </n-anchor-link>
    </n-anchor>
</template>

