<template>
  <div :class="baseClass">
    <slot />
  </div>
</template>
<script lang="ts">
export default {
  name: 'BaseAlert',
  props: {
    variant:{
      type: String,
      default: ''
    }
  },
  computed:{
    baseClass(){
      return ['alert', this.variant ? `alert-${this.variant}`:'']
    }
  }
}
</script>
<style scoped>
.alert {
  background-color: #303030;
  padding: 15px;
  margin: 20px;
  border: 1px solid #969696;
  border-radius: 5px;
  font-family: Arial, sans-serif;
  font-size: 16px;
}
.alert-success {
  background-color: #d4edda;
  color: #155724;
}
.alert-error {
  background-color: #f8d7da;
  color: #721c24;
}

</style>
