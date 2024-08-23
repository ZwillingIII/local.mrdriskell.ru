<template lang="pug">
  button(@click="test") Test
</template>

<script>
import Vue from 'vue';

export default Vue.extend({
  name: 'IndexPage',
  methods: {
    test() {
      fetch('http://localhost/back', {
        method: 'POST'
      })
        .then(response => console.log(response));
    }
  }
})
</script>
