<template>
  <ul>
    <li>
      <playlist-component
        v-for="song in playlist"
        :key="song.id"
        :title="song.title"
        :writer="song.writer"
        :place="song.place"
      ></playlist-component>
    </li>
  </ul>
</template>

<script>
import PlaylistComponent from './components/PlaylistComponent.vue';

export default {
  components: {
    PlaylistComponent,
  },

  data() {
    return {
      playlist: [
        {
          id: 1,
          title: 'Real Estate',
          writer: 'Adam',
          place: 'Avery #1',
        },
        {
          id: 2,
          title: 'The Most Beautiful Thing',
          writer: 'Bruno Major',
          place: 'Avery #1',
        },
      ],
    };
  },
};
</script>
