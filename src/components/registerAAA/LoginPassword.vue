<template>
  <div>
    <slot :row="obj"></slot>
  </div>
</template>

<script>
export default {
  data() {
    return {
      obj: {
        password: '',
        passwordAgin: '',
        invitation: '',
      },
    }
  },
}
</script>

<style></style>
