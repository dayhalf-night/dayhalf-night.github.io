<script lang="ts">
import { NButton, NCard, NSpace } from 'naive-ui';
import { defineComponent } from 'vue';
import abstract from './abstract.vue';
import news from './news.vue';
export default defineComponent({
    components: {
    abstract,
    news,
    NSpace,
    NCard,
    NButton
},
setup(){
    const turnTo = () => {
        window.location.href="#textAnalysis"
    }
    return {
        turnTo
    }
}
})
</script>

<template>
    <n-space>
        <news />
        <n-space vertical>
            <abstract />
            <n-card :bordered="false" title="预测结果">
                真<br />
                模型预测准确率：50%<br />
                <template #footer>
                    <n-button text @click.prevent="turnTo">
                        点击查看可视化视图
                    </n-button>
                </template>
            </n-card>
        </n-space>
    </n-space>
</template>