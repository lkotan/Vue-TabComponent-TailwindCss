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
  name:"Social",
  components:{
    Form,
    SaveButton
  },
  data(){
    return{
       forms: [
        {
          label: "Twitter",
          inputType: "text",
          placeholder: "Twitter",
        },
        {
          label: "Facebook",
          inputType: "text",
          placeholder: "Facebook",
        },
        {
          label: "Google+",
          inputType: "text",
          placeholder: "Google+",
        },
        {
          label: "LinkedIn",
          inputType: "text",
          placeholder: "LinkedIn",
        },
        {
          label: "Instagram",
          inputType: "text",
          placeholder: "LinkedIn",
        },
        {
          label: "YouTube",
          inputType: "text",
          placeholder: "YouTube",
        },
      ],
    }
  }
}
</script>

<style>

</style>