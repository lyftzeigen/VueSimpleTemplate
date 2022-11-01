<script setup lang="ts">
import { useCounterStore } from "@/stores/counter"

const counter = useCounterStore()
</script>

<template>
  <div class="container mx-auto">
    <div class="prose-xl mt-10">
      <h1>This is main page.</h1>

      <p>This is counter object {{ counter }}.</p>

      <p>
        The value is {{ counter.counter }} and its double is
        {{ counter.doubleCount }}.
      </p>

      <div v-on:click="counter.increment()" class="btn btn-primary gap-2">
        <i-carbon-add-alt />
        <span>Increase value</span>
      </div>
    </div>
  </div>
</template>
