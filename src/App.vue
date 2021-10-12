<template>
  <div id="app">
    <h1 class="title">Account Settings</h1>
    <Tabs>
      <Tab name="General" selected="true" icon="user-circle">
        <General />
      </Tab>
      <Tab name="Change Password" icon="unlock-alt">
        <ChangePassword />
      </Tab>
      <Tab name="Information" icon="info-circle">
        <Information />
      </Tab>
      <Tab name="Social" icon="link">
        <Social />
      </Tab>
      <Tab name="Notifications" icon="bell">
        <Notifications />
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
    Notifications,
  },
};
</script>

<style>
body {
  @apply bg-gray-100;
}
#app {
  @apply mt-20
  ml-20
  pb-5
}

#app .title {
  @apply text-3xl
  mb-10
  tracking-wider
  font-extralight
  text-gray-800;
}

@media (max-width: 576px) {
  .general header {
    @apply mr-2;
  }
  .general header div {
    @apply flex
    flex-col
    items-end;
  }
  .general header button {
    @apply w-24
    flex
    justify-center;
  }
  .general .btn-reset {
    @apply mt-2
    ml-4;
  }

  .form-control > div {
    @apply w-full;
  }
  .oldPassword {
    @apply max-w-full;
  }
}

@media (max-width: 768px) {
  #app {
    @apply ml-0;
  }
  #app .title {
    @apply text-center;
  }
}

@media (max-width: 992px) {
   .tab-btn {
    @apply text-center
    text-base
    flex
    justify-center
    items-center
    uppercase
  }
  .checkbox-item p {
    flex-shrink: 12;
  }
}
</style>
