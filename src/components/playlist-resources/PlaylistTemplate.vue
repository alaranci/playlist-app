<template>
  <ul>
    <playlist-component
      v-for="song in playlist"
      :key="song.id"
      :title="song.title"
      :writer="song.writer"
      :place="song.place"
    ></playlist-component>
  </ul>
</template>

<script>
import PlaylistComponent from './PlaylistComponent.vue';

export default {
  props: {
    playlist: Array,
  },

  components: {
    PlaylistComponent,
  },
};
</script>

<style scoped>
ul {
  list-style: none;
  margin: 0;
  padding: 0;
  margin: auto;
  max-width: 40rem;
}
</style>
