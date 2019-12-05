<template>
  <div>
    {{changeMessage}}<hr />
    {{parentMessage}}  
  </div>  
</template>

<script lang="ts">
import {Component, Vue, Prop, Watch} from 'vue-property-decorator';

@Component
export default class Children extends Vue {
  @Prop() parentMessage?: string;

  changeMessage: string = '';

  @Watch('parentMessage')
  messageChange(newVal: string, oldVal: string){
    this.changeMessage = `${newVal} : ${oldVal}`;
  }
}
</script>

<style>

</style>