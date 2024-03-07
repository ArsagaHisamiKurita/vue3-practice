<template>
  <main>
    <button @click="increment">増える</button>
    {{ count }}
  </main>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import { ref } from 'vue'
import TheWelcome from '../components/TheWelcome.vue'

  export default defineComponent({
    components: {
      TheWelcome
    },
    setup() {
      const count = ref(0)

      const increment = () => {
        count.value++
      }

      return {
        count,
        increment
      }
    }
  })
</script>