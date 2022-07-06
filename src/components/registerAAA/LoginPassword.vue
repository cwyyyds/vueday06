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
        password: '哇哇哇哇',
        passwordAgin: '',
        invitation: '',
      },
    }
  },
}
</script>

<style></style>
