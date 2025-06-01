<template>
    <div>
      {{ $route.query.page }}
      <button v-on:click="login()">
          Login
      </button>
    </div>
</template>

<script lang="ts">
export default {
    created() {
        console.log(this.$router)
    },
    methods: {
        login(){
            console.log('logado')
            this.$router.push({name: 'about'})
        }
    }
}
</script>

<style lang="scss" scoped>

</style>
