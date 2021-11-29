<template>
  <li>
    <base-card>
      <header>
        <h3>{{ title }}</h3>
        <base-button mode="flat" @click="removePlaylist(id)"
          >Delete</base-button
        >
      </header>

      <p>{{ writer }}</p>

      <nav>
        <a :href="place">Lihat playlist</a>
      </nav>
    </base-card>
  </li>
</template>

<script>
import BaseCard from '@/components/user-interfaces/BaseCard.vue';
import BaseButton from '@/components/user-interfaces/BaseButton.vue';

export default {
  components: {
    BaseCard,
    BaseButton,
  },

  props: {
    id: String,
    title: String,
    writer: String,
    place: String,
  },

  inject: ['removePlaylist'],
};
</script>

<style scoped>
li {
  margin: auto;
  max-width: 40rem;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

h3 {
  font-size: 1.25rem;
  margin: 0.5rem 0;
}

p {
  margin: 0.5rem 0;
}

a {
  text-decoration: none;
  color: #ce5c00;
}

a:hover,
a:active {
  color: #c89300;
}
</style>
