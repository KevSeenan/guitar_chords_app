<template lang="html">
  <div>
    <ul>
      <SongListItem v-for="(songs, index) in songs" :key="index" :song="songs" />
    </ul>

  </div>
</template>

<script>
import SongListItem from '@/components/SongListItem';

export default {
  name: 'song-list',
  props: ['songs'],
  components: {
    SongListItem
  }
}
</script>

<style lang="css" scoped>
</style>
