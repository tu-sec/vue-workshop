<template>
  <div class="home">
    <p>This is a for loop without a component:</p>
    <ul>
      <li v-for="a in arr" :key="a">{{ a }}</li>
    </ul>

    <p>This is a for loop with a component:</p>
    <NumberComponent v-for="(a, index) in arr" :key="index" :prop="a"></NumberComponent>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import NumberComponent from '@/components/NumberComponent.vue';

@Component({
  components: { NumberComponent }
})
export default class Home extends Vue {
  arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]; // The array we are referencing for the v-for on line 5 and 9
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