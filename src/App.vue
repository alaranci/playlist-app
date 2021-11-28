<template>
  <the-header title="Yahahaha"></the-header>
  <the-resources></the-resources>
  <playlist-template :playlist="playlist"></playlist-template>
</template>

<script>
import TheHeader from '@/components/layouts/TheHeader.vue';
import TheResources from '@/components/playlist-resources/TheResources.vue';
import PlaylistTemplate from '@/components/playlist-resources/PlaylistTemplate.vue';

export default {
  components: {
    TheHeader,
    TheResources,
    PlaylistTemplate,
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
