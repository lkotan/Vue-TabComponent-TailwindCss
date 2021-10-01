<template>
  <div>
      <Form :forms="forms" :checkboxList="true"/>
      <SaveButton/>
  </div>
</template>

<script>
import Form from "@/components/Form"
import SaveButton from "@/components/buttons/SaveButton";
export default {
  name:"Notifications",
  components:{
    Form,
    SaveButton
  },
  data(){
    return{
       forms: [
        {
          text: "Email me when someone comments on my article",
          inputType: "checkbox",
        },
        {
          text: "Email me when someone answers on my form",
          inputType: "checkbox",
        },
        {
          text: "Email me hen someone follows m",
          inputType: "checkbox",
        },
        {
          text: "News and announcements",
          inputType: "checkbox",
        },
        {
          text: "Weekly product updates",
          inputType: "checkbox",
        },
        {
          text: "Weekly blog digest",
          inputType: "checkbox",
        },
      ],
    }
  }
}
</script>

<style>

</style>