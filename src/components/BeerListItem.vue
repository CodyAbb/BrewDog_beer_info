<template lang="html">
  <li v-on:click="handleClick">{{beer.name}}</li>
</template>

<script>
import {eventBus} from '../main.js'

export default {
  name: 'beer-list-item',
  props: ['beer'],
  methods: {
    handleClick(){
      eventBus.$emit('beer-selected', this.beer.id)
    }
  }
}
</script>

<style lang="css" scoped>
</style>
