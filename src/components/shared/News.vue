<template lang="pug">
  transition(name="slideup")
    .alert.alert-warning(v-if="!dismissed", @click="dismissed = true")
      b Work in progress! 
      span Check back for updates!
</template>

<script>
export default {
  name: "News",

  data() {
    return {
      dismissed: false
    }
  }
}
</script>

<style lang="scss" scoped>
.alert {
  margin-bottom: 0;
}

.slideup-leave {
  margin-top: 0;
}

.slideup-leave-active {
  margin-top: -48px; // TODO: better implementation then inspecting the element?
  transition: all 1s ease-in-out;
}
</style>
