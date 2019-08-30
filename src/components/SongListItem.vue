<template lang="html">
  <li @click="handleSongClick">{{song.title}}</li>
</template>

<script>
import{eventBus} from '@/main.js';

export default {
  name: 'song-list-item',
  props: ['song'],
  methods: {
    handleSongClick() {
      eventBus.$emit('song-selected', this.song)
    }
  }
}
</script>

<style lang="css" scoped>
</style>
