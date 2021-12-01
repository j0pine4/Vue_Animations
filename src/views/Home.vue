<template>
  <h1> Home </h1>
  <transition name='fade'>
    <p v-if="show"> Hidden Message </p>
  </transition>
  <button @click="toggle"> Toggle </button>
</template>

<script>
export default {
  data() {
    return {
      show : true
    }
  },
  methods : {
    toggle() {
      this.show = !this.show
    },
  }
}
</script>

<style>

  .fade-enter-from{
    opacity: 0;
  }

  .fade-enter-to{
    opacity: 1;
  }

  .fade-enter-active{
    transition: all 0.4s ease;
  }

  .fade-leave-from{
    opacity: 1;
  }

  .fade-leave-to{
    opacity: 0;
  }

  .fade-leave-active{
    transition: all 0.4s ease;
  }

</style>
