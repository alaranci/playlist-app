<template>
  <the-header title="Yahahaha"></the-header>
  <playlist-template :playlist="playlist"></playlist-template>
</template>

<script>
import PlaylistTemplate from '@/components/playlist-resources/PlaylistTemplate.vue';
import TheHeader from '@/components/layouts/TheHeader.vue';

export default {
  components: {
    PlaylistTemplate,
    TheHeader,
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

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

* {
  box-sizing: border-box;
}

html {
  font-family: 'Roboto', sans-serif;
}

body {
  margin: 0;
}
</style>
