

<template>
  <div>
    <BaseAlert :variant="variant">
      {{ texto }}
    </BaseAlert>
  </div>
  <div @click="changeVariant">
    <BaseCard/>
  </div>
</template>
<!-- eslint-disable vue/block-lang -->
<script>
import BaseAlert from '@/components/BaseAlert.vue';
import BaseCard from '@/components/BaseCard.vue';

export default {
  name: 'App',
  components: {
    BaseAlert,
    BaseCard,
  },
  data() {
    return {
      variant: 'error',
      texto: 'erro'
    }
  },
  methods: {
    changeVariant(event) {
      console.log(event);
      this.variant = this.variant === 'error' ? 'success' : 'error';
      if(this.variant === 'error'){
        this.texto = 'Há um erro no retorno'
      }else{
        this.texto = 'Sucesso no envio'
      }

      console.log(this.variant);

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
