<template lang="html">
  <div>
    <p>{{song.name}}</p>
    <p>{{song.artist}}</p>
    <p>{{song.tabTypes}}</p>
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
