
<template>
  <content-card row transparent wrap>
    <template v-slot:content>
      <content-card v-for="(s,i) in streamArray" :rows="3" :key="i">
        <template v-slot:content>
          <video-container ref="video" :url="s" />
        </template>
      </content-card>
    </template>
  </content-card>
</template>

<script>
import ContentCard from '../ContentCard'
import VideoContainer from '../VideoContainer'
import BoxMixin from './BoxMixin'

export default {
  name: 'NineGridBox',
  components: { VideoContainer, ContentCard },
  mixins: [BoxMixin]
}
</script>

<style scoped>

</style>
