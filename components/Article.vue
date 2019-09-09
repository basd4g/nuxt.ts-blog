<template>
    <div>{{articleId}}</div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component
export default class Article extends Vue {
    @Prop({ type: String, required: true })
    articleId: String
}
</script>