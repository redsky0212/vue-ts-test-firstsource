<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <message />
  </div>
</template>

<script lang="ts">
// @ is an alias to /src
import message from '@/components/message.vue';

export default {
 components: {
    message,
  },
};
</script>
