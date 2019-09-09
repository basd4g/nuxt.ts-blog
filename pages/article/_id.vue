<template>
    <div>
        <Article v-bind:articleId="$route.params.id"></Article>
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
}
</script>
 