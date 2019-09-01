<template lang="html">
  <div>
    <h3>Bob Dylan</h3>
    <label for="song-selected">Select A Song:</label>
    <!-- <select v-model="songs" v-on:change="handleChange">
      <option disabled value=" ">Select A Song</option>
      <option v-for="(song, index) in songs" :value="songs" :key="index">{{song.title}}</option>
    </select> -->

    <ul>
      <SongListItem v-for="(songs, index) in songs" :key="index" :song="songs" />
    </ul>

  </div>
</template>

<script>

import SongListItem from '@/components/SongListItem';

import {eventBus} from '../main.js';

export default {
  name: 'song-list',
  props: ['songs'],
  // methods: {
  //   handleChange() {
  //     eventBus.$emit('song-selected', this.song)
  //   },
    components: {
      SongListItem
    }
  }
// }


</script>

<style lang="css" scoped>
</style>
