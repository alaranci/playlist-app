<template>
  <base-card>
    <base-button @click="setSelectedTab('playlist-component')"
      >Playlist</base-button
    >
    <base-button @click="setSelectedTab('add-resources')"
      >Add Resource</base-button
    >
  </base-card>
  <component :is="selectedTab"></component>
</template>

<script>
import PlaylistComponent from './PlaylistComponent.vue';
import AddResources from './AddResources.vue';
import BaseButton from '../user-interfaces/BaseButton.vue';
import BaseCard from '../user-interfaces/BaseCard.vue';

export default {
  components: {
    PlaylistComponent,
    AddResources,
    BaseButton,
    BaseCard,
  },

  data() {
    return {
      selectedTab: 'playlist-template',
    };
  },

  methods: {
    setSelectedTab(tab) {
      this.selectedTab = tab;
    },
  },
};
</script>
