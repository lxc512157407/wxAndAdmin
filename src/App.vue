<template>
  <div id="app">
    <test />
    <router-view />
    <service-worker-update-popup />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import ServiceWorkerUpdatePopup from '@/pwa/components/ServiceWorkerUpdatePopup.vue'
import test from '@/publicComponents/test.vue'

@Component({
  name: 'App',
  components: {
    ServiceWorkerUpdatePopup,
    test
  }
})
export default class extends Vue {}
</script>
