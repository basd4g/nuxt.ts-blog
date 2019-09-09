<template>
    <div>{{articleId}}</div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component
export default class Article extends Vue {
    @Prop({ type: String,required: true })
    articleId!: String
}
/*
    asyncData(){
        return {
            obj : require('~/assets/article/sample-article1/index.json')
            //requireでjsonを読み込みたい
        }
    }
*/
</script>