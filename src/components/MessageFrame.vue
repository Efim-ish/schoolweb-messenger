<template>
  <div class="message-frame user-frame">
    <p class="message-frame__header">
      From: {{ getUserNameById(msg.from) }}
    </p>
    <p class="message-frame__header">
      To: {{ getUserNameById(msg.to) }}
    </p>
    <p>{{ msg.content }}</p>
  </div>
</template>

<script>
export default {
  props: ["msg", "users"],
  methods: {
    getUserNameById(id) {
      return this.users.find((user) => user.id === id)?.name;
    },
  },
};
</script>

<style>
.message-frame {
  font-family: Arial, Helvetica, sans-serif;
  max-width: 400px;
  padding: 10px;
  margin-bottom: 30px;
  border: 1px solid lightgray;
  border-radius: 10px;
  box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.15);
}

.message-frame__header {
  border-bottom: 1px dashed lightgray;
  font-weight: bold;
  padding-bottom: 5px;
}
</style>