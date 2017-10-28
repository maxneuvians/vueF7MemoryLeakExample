<template>
  <!-- App -->
  <div id="app">
    <!-- Statusbar -->
    <f7-statusbar></f7-statusbar>

    <!-- Main Views -->
    <f7-views>
      <f7-view id="main-view" main>
        <!-- Pages -->
        <f7-pages>
          <f7-page>
            <div>
              <p>Is component active? {{showHog}}</p>
              <button v-on:click="toggleHog()">Toggle List</button>
              <hog v-if="showHog"></hog>
            </div>
          </f7-page>
        </f7-pages>
      </f7-view>
    </f7-views>
  </div>
</template>

<script>
import hog from './pages/hog.vue';

export default {
  name: 'app',
  components: {
    'hog': hog
  },
  data() {
    return {
      showHog: false
    }
  },
  methods: {
    toggleHog(){
      this.showHog = !this.showHog
    }
  }
}
</script>
