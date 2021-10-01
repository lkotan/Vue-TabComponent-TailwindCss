<template>
  <div id="app">
    <h1 class="title">Account Settings</h1>
    <Tabs>
      <Tab name="General" selected="true" icon="user-circle">
        <General/>
      </Tab>
      <Tab name="Change Password" icon="unlock-alt">
       <ChangePassword/>
      </Tab>
      <Tab name="Information" icon="info-circle">
       <Information/>
      </Tab>
      <Tab name="Social" icon="link">
        <Social />
      </Tab>
      <Tab name="Notifications" icon="bell">
        <Notifications/>
      </Tab>
    </Tabs>
  </div>
</template>

<script>
import Tabs from "@/components/Tabs";
import Tab from "@/components/Tab";
import General from "@/components/account/General";
import ChangePassword from "@/components/account/ChangePassword";
import Information from "@/components/account/Information";
import Social from "@/components/account/Social";
import Notifications from "@/components/account/Notifications";

export default {
  name: "App",
  components: {
    Tabs,
    Tab,
    General,
    Information,
    ChangePassword,
    Social,
    Notifications
  },
};
</script>

<style>
body{
@apply

  bg-gray-100
}
#app{
  @apply

  mt-20
  ml-20
}

#app .title{
  @apply

  text-3xl
  mb-10
  tracking-wider
  font-extralight
  text-gray-800
}

</style>
