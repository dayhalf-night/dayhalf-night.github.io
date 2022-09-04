<script lang="ts">

import ChevronDoubleDown16Regular from '@vicons/fluent/ChevronDoubleDown16Regular'
import type { AnchorInst } from 'naive-ui'
import { NAnchor, NButton, NButtonGroup, NIcon } from 'naive-ui'
import { defineComponent, ref } from 'vue'

  
  export default defineComponent({
    components: {
      NButton,
      NAnchor,
      NIcon,
      NButtonGroup,
      ChevronDoubleDown16Regular
    },
    setup () {
      const anchorRef = ref<AnchorInst | null>(null)
      const scrollTo = (href: string) => {
        anchorRef.value?.scrollTo(href)
      }
      const turnTo = () => {
        window.location.href="#calculate"
      }
      return {
        anchorRef,
        scrollTo,
        turnTo
      }
    }
  })
  </script>
    
<template>
    <h1>虚假新闻检测系统</h1>
    <br />
    <n-button-group vertical >
    <n-button text @click.prevent="turnTo">
      点击进入
    </n-button>
    <n-button text>
      <template #icon>
      <n-icon>
        <ChevronDoubleDown16Regular />
      </n-icon>
      </template>
    </n-button>
  </n-button-group>
</template>

    