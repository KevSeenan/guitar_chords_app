<template lang="html">
  <div>
    <p>Song Title:{{song.title}}</p>
    <p>Artist:{{song.artist.name}}</p>
    <p>Tab Type:{{song.tabTypes}}</p>
    <p>Find Tab: http://www.songsterr.com/a/wa/bestMatchForQueryString?s={{song.title}}&a={{song.artist.name}}</p>
  </div>
</template>

<script>
export default {
  name: 'song-detail',
  props: ['song']
}
</script>

<style lang="css" scoped>

</style>
