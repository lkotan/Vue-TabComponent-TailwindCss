<template>
  <div class="general">
    <header>
      <img src="@/assets/user.png" alt="" />
      <div>
        <Button class="btn-upload" name="Upload" />
        <Button class="btn-reset" name="Reset" />
        <p>Allowed JPG, GIF or PNG. Max size of 800kB</p>
      </div>
    </header>
    <Form :forms="forms" />
    <SaveButton />
  </div>
</template>

<script>
import Button from "@/components/buttons";
import SaveButton from "@/components/buttons/SaveButton";
import Form from "@/components/Form";
export default {
  name: "General",
  components: {
    Button,
    SaveButton,
    Form,
  },
  data() {
    return {
      forms: [
        { label: "Username", inputType: "text", placeholder: "Username" },
        { label: "Name", inputType: "text", placeholder: "Name" },
        { label: "Email", inputType: "email", placeholder: "Email" },
        { label: "Company", inputType: "text", placeholder: "Company" },
      ],
    };
  },
};
</script>

<style>
.general header {
  @apply flex
  items-center
  mt-4 ml-6;
}
.general header div {
  @apply ml-6;
}
.general header p {
  @apply ml-4
  mt-3
  text-lg
  tracking-wider
  font-light;
}
.general img {
  @apply w-24
  h-24
  rounded-md;
}
.general .btn-upload {
  @apply ml-4
  hover:shadow-lg
  bg-purple-500;
}
.general .btn-reset {
  @apply ml-2
  border
  hover:bg-gray-50
  border-black
  bg-white
  text-black;
}
</style>
