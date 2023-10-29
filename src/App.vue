<script setup>
import HelloWorld from "./components/HelloWorld.vue";
import TabsComponent from "./components/TabsComponent.vue";
</script>

<template>
  <!-- <TabsComponent /> -->
  <div class="flex flex-col">
    <div class="flex absolute top-4">
      <img
        alt="Vue logo"
        class="logo"
        src="./assets/logo.svg"
        width="125"
        height="125"
      />

      <div class="wrapper">
        <HelloWorld msg="You did it!" />
      </div>
    </div>

    <div class="flex w-full pt-10">
      <TabsComponent />
    </div>
  </div>
</template>

<style scoped></style>
