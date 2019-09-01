<template lang="html">
  <div>
    <li @click="handleSongClick">{{song.title}}</li>
  </div>
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

li:hover {
  background: red;
  text-transform: uppercase;
  color: white;
  cursor: pointer;
}

li {
  text-decoration: underline;
  list-style: none;
}

</style>
