<template>
  <div id="app">
    <test />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import test from '@/publicComponents/test.vue'
@Component({
  name: 'App',
  components: {
    test
  }
})
export default class extends Vue {}
</script>
