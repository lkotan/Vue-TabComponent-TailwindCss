<template>
  <div>
      <Form :forms="forms"/>
      <SaveButton/>
  </div>
</template>

<script>
import Form from "@/components/Form"
import SaveButton from "@/components/buttons/SaveButton";
export default {
  name:"Information",
  components:{
    Form,
    SaveButton
  },
  data(){
    return{
       forms: [
        {
          label: "Bio",
          inputType: "textarea",
          placeholder: "Your bio data here",
        },
        {
          label: "City",
          inputType: "text",
          placeholder: "City",
        },
        {
          label: "Country",
          inputType: "text",
          placeholder: "Country",
        },
        {
          label: "Website",
          inputType: "text",
          placeholder: "Website",
        },
        {
          label: "Phone",
          inputType: "number",
          placeholder: "Phone",
        },
      ],
    }
  }
}
</script>

<style>

</style>