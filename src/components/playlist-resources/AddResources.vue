<template>
  <base-dialog
    v-if="isInputInvalid"
    title="Invalid Input"
    @close="isInputInvalid = false"
  >
    <template #default>
      <p>Unfortunately, at least one input value is invalid</p>
      <p>
        Please check all inputs and make sure you enter at least a few
        characters into each input field
      </p>
    </template>
    <template #actions>
      <base-button @click="isInputInvalid = false">Okay</base-button>
    </template>
  </base-dialog>
  <base-card>
    <form @keyup.enter="fetchUserInput">
      <div class="form-control">
        <label for="title"
          >Title: <input type="text" id="title" v-model="userInput.title"
        /></label>
      </div>
      <div class="form-control">
        <label for="writer"
          >Writer: <input type="text" id="writer" v-model="userInput.writer"
        /></label>
      </div>
      <div class="form-control">
        <label for="place"
          >Place:
          <textarea type="url" id="place" rows="3" v-model="userInput.place" />
        </label>
      </div>
      <base-button type="submit" @click.prevent="fetchUserInput"
        >Add Playlist</base-button
      >
    </form>
  </base-card>
</template>

<script>
import BaseButton from '../user-interfaces/BaseButton.vue';
import BaseCard from '../user-interfaces/BaseCard.vue';
import BaseDialog from '../user-interfaces/BaseDialog.vue';

export default {
  components: {
    BaseCard,
    BaseButton,
    BaseDialog,
  },

  inject: ['addPlaylist'],

  data() {
    return {
      userInput: {
        title: '',
        writer: '',
        place: '',
      },
      isInputInvalid: false,
    };
  },

  methods: {
    fetchUserInput() {
      const title = this.userInput.title;
      const writer = this.userInput.writer;
      const place = this.userInput.place;

      if (title.trim() !== '' && writer.trim() !== '' && place.trim() !== '') {
        this.addPlaylist(title, writer, place);
      } else {
        this.isInputInvalid = true;
      }
    },
  },
};
</script>

<style scoped>
label {
  font-weight: bold;
  display: block;
  margin-bottom: 0.5rem;
}

input,
textarea {
  display: block;
  width: 100%;
  font: inherit;
  padding: 0.15rem;
  border: 1px solid #ccc;
}

input:focus,
textarea:focus {
  outline: none;
  border-color: #3a0061;
  background-color: #f7ebff;
}

.form-control {
  margin: 1rem 0;
}
</style>
