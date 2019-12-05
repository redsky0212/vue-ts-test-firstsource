<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <message />
    <children :parentMessage="message" />
    <button @click="onChange">change</button>
  </div>
</template>

<script lang="ts">
import {Component, Vue} from 'vue-property-decorator';
// @ is an alias to /src
import message from '@/components/message.vue';
import children from '@/components/children.vue';

@Component({
  components: {
    message,
    children,
  },
})
export default class Home extends Vue {
  message: string = 'fjdsalkfjdskal';

  onChange() {
    this.message = '내용 바꾸기!!';
  }
}
</script>
