<template>
    <div>
      <Article v-bind:articleId="$route.params.id" v-bind:articleObject="articleObject"></Article>
    </div>
   
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import Article from '~/components/Article.vue'

@Component({
  components: {
    Article
  }
})
export default class Index extends Vue {
  articleObject: Object = {
    "title": "",
    "date": "",
    "tags": "",
    "bodyContent": "",
    "bodyHtml": "",
    "dir": "",
    "base": "",
    "ext": "",
    "sourceBase": "",
    "sourceExt": ""
  }
  async asyncData ({ params }){
    let articleObject = await require('~/assets/article/sample-article1/index.json')
    console.log(articleObject)
    return { articleObject }
  }
}

/*
    
*/
</script>
 