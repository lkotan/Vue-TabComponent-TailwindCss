<template>
  <div>
    <Form :forms="forms" />
    <SaveButton />
  </div>
</template>

<script>
import Form from "@/components/Form";
import SaveButton from "@/components/buttons/SaveButton";
export default {
  name: "ChangePassword",
  components: {
    Form,
    SaveButton
  },
  data() {
    return {
      forms: [
        {
          label: "Old Password",
          inputType: "password",
          placeholder: "Old Password",
        },
        {
          label: "New Password",
          inputType: "password",
          placeholder: "New Password",
        },
        {
          label: "Retype New Password",
          inputType: "password",
          placeholder: "Retype New Password",
        },
      ],
    };
  },
};
</script>

<style></style>
