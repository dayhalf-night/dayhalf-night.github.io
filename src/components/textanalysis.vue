<script lang="ts">
    import { NCard } from 'naive-ui';
import { defineComponent } from 'vue';

    export default defineComponent({
        components:{
            NCard
        }
    })
</script>

<template>
    <n-card title="关键词可视化">
        <img src="../assets/wordcloud.png" style="height:80%">
    </n-card>
</template>

<style scoped>
    .n-card{
        max-height: 500px;
    }
</style>