<template>
  <button class="btn">{{ name }}</button>
</template>

<script>
export default {
  name: "Button",
  props: {
    name: { required: true },
  },
};
</script>

<style>
.btn {
  @apply rounded-md
     px-4 py-1
      outline-none
      duration-500
      text-sm
     text-white
}
</style>
