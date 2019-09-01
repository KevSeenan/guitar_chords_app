<template lang="html">
  <div id="view" v-if="songs.length">
    <SongList :songs="songs" />
    <SongDetail v-if="selectedSong":song="selectedSong" />
  </div>
</template>

<script>
import SongList from '@/components/SongList';
import SongDetail from '@/components/SongDetail';
import {eventBus} from '@/main.js';

export default {
  name: 'song-view',
  data () {
    return{
      songs: [],
      selectedSong: null
    }
  },
  mounted() {
    fetch('https://www.songsterr.com/a/ra/songs.json?pattern=Dylan')
    .then(res => res.json())
    .then(songs => this.songs = songs)

    eventBus.$on('song-selected', (song) => {
      this.selectedSong = song;
    })
  },
  components: {
    SongList,
    SongDetail
  }
}
</script>

<style lang="css" scoped>

#view {
  display:flex;
  cursor: pointer;
  color: 	#FF4500;
  /* background-color: #000000; */
  background-image: url('../assets/me_jamming.jpg');
  background-repeat: no-repeat;
  background-size: cover;
}

</style>
