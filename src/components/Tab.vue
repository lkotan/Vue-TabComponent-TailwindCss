<template>
  <div v-if="isActive">
    <slot />
  </div>
</template>

<script>
export default {
  name: "Tab",
  props: {
    name: { required: true },
    icon:{required:true},
    selected: { required: false },
  },
  data() {
    return {
      isActive: false,
    };
  },
  mounted() {
    this.isActive = this.selected;
  },
};
</script>

<style></style>
