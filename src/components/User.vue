<template setup>
  <div>
    {{ this.$route.params.userId }}
  </div>
</template>
<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "User",
  created() {
    console.log(this.$route.params.userId);
  }
}
</script>
<style lang="">
  
</style>