<template lang="pug">
  div
    button(@click="test") {{ btnTxt }}
    div(v-if="errorTxt.length") {{ errorTxt }}
</template>

<script>
import Vue from 'vue';
import axios from "axios";

export default Vue.extend({
  name: 'IndexPage',
  data() {
    return {
      btnTxt: 'Test',
      errorTxt: ''
    }
  },
  methods: {
    test() {
      let data = this;

      data.errorTxt = '';

      axios.post('http://localhost/api/test')
        .then(function (response) {
          data.btnTxt = response.data[0];
        })
        .catch(function (error) {
          data.errorTxt = error.message;
        })
    }
  }
})
</script>
