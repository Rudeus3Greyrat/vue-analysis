<template>
  <button @click="toggleContent">
    {{ show }}
  </button>
</template>
<script lang="ts" setup>
import {computed, ref} from "vue";

const count = ref('Hello World')
const show=computed(()=>count.value+' from Greyrat')
function toggleContent() {
  count.value === 'Hello Vue'?count.value='Hello World':count.value='Hello Vue'
}
</script>