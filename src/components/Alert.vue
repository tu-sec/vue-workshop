<template>
    <div>
        <button @click="emitEvent()">Click Me!</button>
    </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class Alert extends Vue {
    val = false;

    /**
     * Changes a internal component variable and emits a new event
     */
    emitEvent() {
        this.val = !this.val;
        this.$emit('myEvent', this.val);
    }
}
</script>
