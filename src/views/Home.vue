<template>
  <div class="home">
    <oprosnik />
  </div>
</template>

<script>
// @ is an alias to /src
import oprosnik from '@/components/oprosnik.vue'

export default {
  name: 'Home',
  components: {
    oprosnik
  }
}
</script>
