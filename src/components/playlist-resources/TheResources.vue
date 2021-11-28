<template>
  <base-card>
    <base-button
      @click="setSelectedTab('playlist-template')"
      :mode="selectedTab === 'playlist-template' ? null : 'flat'"
      >Playlist</base-button
    >
    <base-button
      @click="setSelectedTab('add-resources')"
      :mode="selectedTab === 'add-resources' ? null : 'flat'"
      >Add Resource</base-button
    >
  </base-card>
  <component :is="selectedTab"></component>
</template>

<script>
import PlaylistTemplate from './PlaylistTemplate.vue';
import AddResources from './AddResources.vue';
import BaseButton from '../user-interfaces/BaseButton.vue';
import BaseCard from '../user-interfaces/BaseCard.vue';

export default {
  components: {
    PlaylistTemplate,
    AddResources,
    BaseButton,
    BaseCard,
  },

  provide() {
    return {
      playlist: this.playlist,
    };
  },

  data() {
    return {
      selectedTab: 'playlist-template',
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

  methods: {
    setSelectedTab(tab) {
      this.selectedTab = tab;
    },
  },
};
</script>
