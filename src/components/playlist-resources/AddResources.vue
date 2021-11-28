<template>
  <base-card>
    <form>
      <div class="form-control">
        <label for="title">Title: <input type="text" id="title" /></label>
      </div>
      <div class="form-control">
        <label for="writer">Writer: <input type="text" id="writer" /></label>
      </div>
      <div class="form-control">
        <label for="place"
          >Place: <textarea type="url" id="place" rows="3" />
        </label>
      </div>
      <base-button type="submit">Add Playlist</base-button>
    </form>
  </base-card>
</template>

<script>
import BaseButton from '../user-interfaces/BaseButton.vue';
import BaseCard from '../user-interfaces/BaseCard.vue';

export default {
  components: {
    BaseCard,
    BaseButton,
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
