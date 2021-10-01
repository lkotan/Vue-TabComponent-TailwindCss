<template>
  <div class="tabs">
    <header class="tabs-header">
      <div v-for="(tab, index) in tabs" :key="index">
        <button
          class="tab-btn"
          @click="changeTab(tab)"
          :class="{ 'is-active': tab.isActive }"
        >
          <font-awesome-icon :icon="tab.icon" />
          {{ tab.name }}
        </button>
      </div>
    </header>
    <section class="tabs-details fitContent">
      <slot></slot>
    </section>
  </div>
</template>

<script>
export default {
  name: "Tabs",
  data() {
    return {
      tabs: [],
    };
  },
  created() {
    this.tabs = this.$children;
  },
  methods: {
    changeTab(tab) {
      this.tabs.forEach((item) => {
        item.isActive = item.name == tab.name;
      });
    },
  },
};
</script>

<style>
.tabs {
  @apply flex;
}
.tabs .tabs-header {
  @apply flex-shrink-0;
}
.tabs .tab-btn {
  @apply w-56
    border-none
    outline-none
    mb-2
    p-2
    rounded-md
    text-left
    text-lg
    font-medium;
}
.tabs svg {
  @apply mr-3;
}
.is-active {
  @apply text-white
  shadow-xl
  bg-indigo-600;
}
.tabs-details {
  @apply flex-auto
    mx-10
    shadow-xl
    rounded-md
    bg-white
}
</style>
