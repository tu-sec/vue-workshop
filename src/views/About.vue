<template>
  <div class="home">
    <p>About Page</p>
    <button @click="goToHome()">Go to Home</button>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class About extends Vue {
    /**
     * Rolls back the router history to go to home
     */
    goToHome() {
        this.$router.back();
    }
}
</script>

<style lang="scss" scoped>
.home {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>