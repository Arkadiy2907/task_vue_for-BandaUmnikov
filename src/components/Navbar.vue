<template>
  <div class="navbar">
    <my-button @click="getRandomCard">случайный выбор кафе</my-button>
    <my-button @click="fetchPosts">все варианты кафе</my-button>
    <my-button @click="sendSelectedObject">
      отправить выбранное на почту
    </my-button>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },

  props: {
    onGetRundomCard: Function,
    onFetchPosts: Function,
    onSendSelectedObject: Function,
  },

  methods: {
    getRandomCard() {
      this.$emit("onGetRandomCard", null);
    },
    fetchPosts() {
      this.$emit("onFetchPosts", null);
    },
    sendSelectedObject() {
      this.$emit("onSendSelectedObject", null);
    },
  },
};
</script>
