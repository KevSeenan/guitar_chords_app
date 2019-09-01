<template lang="html">
  <div id="view">
    <Header />
    <SongView />
  </div>
</template>

<script>

import Header from '@/components/Header';
import SongView from '@/components/SongView';
import SongDetail from '@/components/SongDetail';

export default {
  name: 'app',
  components: {
    Header,
    SongView,
    SongDetail
  }
}
</script>

<style lang="css" scoped>
#view{
  border-style: groove;
}
</style>
