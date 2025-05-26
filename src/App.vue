

<template>
  <div>
    <BaseAlert v-if="showAlert" :variant="variant" @close="onClose">
      {{ texto }}
    </BaseAlert>
  </div>
  <div >
  </div>
</template>
<!-- eslint-disable vue/block-lang -->
<script>
import BaseAlert from '@/components/BaseAlert.vue';

export default {
  name: 'App',
  components: {
    BaseAlert,
  },
  data() {
    return {
      showAlert: true,
      variant: 'error',
      texto: 'erro'
    }
  },
  methods: {
    onClose(){
      this.showAlert = false
      console.log("fechado aq")
    }
  },
  watch: {
  },
  computed: {
  },
  beforeCreate() {
  },
  created() {
  },
  beforeMount() {
  },
  mounted() {
  },
  beforeUnmount() {
  },
  unmounted() {
  },

}
</script>
<style scoped>



</style>
