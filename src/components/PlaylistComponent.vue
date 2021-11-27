<template>
  <div class="header">
    <h2>{{ title }}</h2>
    <button>Delete</button>
  </div>
  <div class="content">
    <p>{{ writer }}</p>
  </div>
  <div class="footer">
    <span>{{ place }}</span>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    writer: String,
    place: String,
  },
};
</script>
