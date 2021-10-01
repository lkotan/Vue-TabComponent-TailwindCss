<template>
  <button class="btn btn-save">{{ name }}</button>
</template>

<script>
export default {
  name: "SaveButton",
  props: {
    name: { default: "Save Changes" },
  },
};
</script>

<style>
.btn-save {
  @apply mt-5 mb-3 mr-7 ml-auto
  font-semibold
  flex
  hover:shadow-2xl
  bg-purple-500;
}
</style>
