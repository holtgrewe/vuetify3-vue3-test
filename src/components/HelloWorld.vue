<script setup lang="ts">
import { ref } from 'vue'

interface Props {
  msg: string
}

const props = defineProps<Props>()

const msg = ref(`The message is: ${props.msg}`)
</script>

<template>
  <h1 class="text-h2 font-weight-bold">
    {{ msg }}
  </h1>

  <v-btn
    id="button"
    @click="() => msg = 'AFTER CHANGE'"
  >
    CHANGE ME
  </v-btn>
</template>
