<template>
  <div class="home">
    <button @click="toggleVisible()">Toggle Visibility</button>
    <p v-if="visible">Welcome to your first Vue App!</p>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class Home extends Vue {
  visible = false; // Variable referenced in the v-if on line 4

  /**
   * Toggles the visibility on and off of the welcome message
   * 
   * Used by the click handler on line 3
   */
  toggleVisible(): void {
    this.visible = !this.visible;
  }
}
</script>

<style lang="scss" scoped>
button {
  display: block;
  margin-bottom: 20px;
}
.home {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>