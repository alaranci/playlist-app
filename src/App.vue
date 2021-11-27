<template>
  <ul>
    <li v-for="song in playlist" :key="song.id">
      <h2>{{ song.title }}</h2>
      <p>{{ song.writer }}</p>
      <span>{{ song.place }}</span>
    </li>
  </ul>
</template>

<script>
export default {
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
