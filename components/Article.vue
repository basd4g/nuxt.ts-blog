<template>
    <div>{{articleId}}
        <span v-html="articleObject.bodyHtml"></span>
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

type ArticleObject = {
  title : string
  date : string,
  tags : string,
  bodyContent: string,
  bodyHtml: string,
  dir: string,
  base: string,
  ext: string,
  sourceBase: string,
  sourceExt: string
}

@Component
export default class Article extends Vue {
    @Prop({ type: String,required: true })
    articleId!: String

    @Prop({ type: Object,required: true })
    articleObject!: Object
}

</script>