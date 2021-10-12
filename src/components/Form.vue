<template>
  <div class="form">
    <div class="form-control" v-if="!checkboxList">
      <div
        v-for="item in forms"
        :key="item.label"
        :class="[
          item.label == 'Old Password' ? 'oldPassword' : '',
          item.inputType == 'textarea' ? 'wfull' : '',
        ]"
      >
        <label>{{ item.label }}</label>
        <textarea
          rows="3"
          v-if="item.inputType == 'textarea'"
          :placeholder="item.placeholder"
        ></textarea>
        <input v-else :type="item.inputType" :placeholder="item.placeholder" />
      </div>
    </div>
    <div v-else class="checkbox-list">
      <div class="checkbox-item" v-for="item in forms" :key="item.text">
        <label class="switch">
          <input
            type="checkbox"
            :checked="item.text.length > 25 ? true : false"
          />
          <span class="slider round"></span>
        </label>
        <p>
          {{ item.text }}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Form",
  props: {
    forms: { required: true },
    checkboxList: { default: false },
  },
};
</script>

<style>
.form {
  @apply mx-2;
}
.form-control {
  @apply flex
    flex-wrap;
}
.form-control > div {
  @apply w-1/2
  px-4;
}
.form input,
.form textarea {
  @apply w-full
  p-2
  rounded-md
  border
  outline-none
  border-gray-300
  duration-300
  focus:border-indigo-600
  focus:shadow-lg;
}
.form label {
  @apply block
  mt-4
  text-sm;
}
.oldPassword,
.wfull {
  @apply w-full !important;
}
.oldPassword {
  max-width: 50.01%;
}

.checkbox-list {
  @apply m-6;
}
.checkbox-item {
  @apply flex
    items-center;
}
.checkbox-item p {
  @apply mt-4
    ml-2;
}
.switch {
  @apply relative
    w-12
    h-5;
}

.switch input {
  @apply opacity-0
    w-0
    h-0;
}

.slider {
  @apply absolute
    cursor-pointer
    top-0
    left-0
    right-0
    bottom-0
    bg-gray-400
    duration-500;
}

.slider:before {
  bottom: 2.6px;
  content: "";
  @apply absolute
    h-4
    w-4
    left-1
    bg-white
    duration-500;
}

input:checked + .slider {
  @apply bg-blue-600;
}

input:focus + .slider {
  @apply shadow-xl;
}

input:checked + .slider:before {
  @apply transform
  translate-x-6;
}

.slider.round {
  @apply rounded-3xl;
}

.slider.round:before {
  @apply rounded-full;
}

</style>
