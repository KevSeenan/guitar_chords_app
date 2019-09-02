<template lang="html">
  <div id="song-list">
    <h3>Bob Dylan</h3>
    <!-- <label for="artist-select">Select An Artist:</label> -->
    <!-- <select v-model="artists" v-on:change="">
      <option disabled value=" ">Select An Artist</option>
      <option SongListItem v-for="(artist, index) in artists" :value="artists" :key="index">{{song.artist}}</option>
    </select> -->

    <label for="song-selected">Select A Song:</label>
    <!-- <select v-model="songs" v-on:change="handleChange">
      <option disabled value=" ">Select A Song</option>
      <option SongListItem v-for="(song, index) in songs" :value="songs" :key="index">{{song.title}}</option>
    </select> -->
    <select v-model="songs" v-on:change="">
      <option disabled value=" ">Select A Song</option>
      <option SongListItem v-for="(song, index) in songs" :value="songs" :key="index">{{song.title}}</option>
    </select>

    <ul>
      <SongListItem v-for="(songs, index) in songs" :key="index" :song="songs" />
    </ul>

  </div>
</template>

<script>

import SongListItem from '@/components/SongListItem';
// import SongDetail from '@/components/SongDetail';

import {eventBus} from '../main.js';

export default {
  name: 'song-list',
  props: ['songs'],
  // methods: {
  //   handleChange() {
  //     eventBus.$emit('song-selected', this.song)
  //   },
    components: {
      SongListItem,
      // SongDetail
    }
  }
// }


</script>

<style lang="css" scoped>

#song-list{
  border-style: groove;
  overflow: scroll;
  height: 100vh;
}

h3 {
  text-decoration: underline;
}

label, select {
  display: grid;
}
</style>
