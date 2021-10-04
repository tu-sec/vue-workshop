<template>
  <div class="home">
    <Alert @myEvent="handleEvent($event)" />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Alert from '@/components/Alert.vue';

@Component({
  components: { Alert },
})
export default class Home extends Vue {
  // Good for before DOM renders
  created() {
    window.alert('Created');
  }

  // Good for after DOM renders
  mounted() {
    window.alert('Mounted');
  }

  /**
   * Takes the event from the Alert component and creates
   * a new window alert
   */
  handleEvent(val: boolean) {
    window.alert(`Value is ${val}`);
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