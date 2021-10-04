<template>
  <div>
    This component's number is {{ prop }}
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class NumberComponent extends Vue {
  @Prop({ required: false })
  prop: number | undefined;
}
</script>