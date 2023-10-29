<template>
  <div class="flex flex-col w-[700px]">
    <div
      class="text-base font-medium border-b-2 border-[#D9D9D9] dark:text-gray-400 dark:border-gray-700"
    >
      <ul class="flex justify-between -mb-px">
        <li
          class="inline-block p-4 cursor-pointer hover:text-gray-600"
          @click="toggleTabs(1)"
          :class="{
            ' border-b-4 border-blue-800 font-medium': openTab === 1,
          }"
        >
          Home
        </li>
        <li
          class="inline-block p-4 cursor-pointer hover:text-gray-600"
          @click="toggleTabs(2)"
          :class="{
            'border-b-4 border-borderBlue font-medium': openTab === 2,
          }"
        >
          Profil
        </li>
        <li
          class="inline-block p-4 cursor-help hover:text-gray-600"
          :class="{
            'border-b-4  border-blue-800 font-medium': openTab === 3,
          }"
        >
          Setting
        </li>
      </ul>
    </div>

    <div class="tab-content pt-5">
      <div
        class="overflow-auto max-h-[194px]"
        :class="{ hidden: openTab !== 1, block: openTab === 1 }"
      >
        <p class="text-base font-medium w-[400px] xl:w-[450px]">
          Tab Setting Home
        </p>
      </div>
      <div
        class="overflow-auto max-h-[194px]"
        :class="{ hidden: openTab !== 2, block: openTab === 2 }"
      >
        <p class="text-base font-medium w-[400px] xl:w-[450px]">
          Tab Setting Profil
        </p>
      </div>
      <div
        class="overflow-auto max-h-[194px]"
        :class="{ hidden: openTab !== 3, block: openTab === 3 }"
      >
        <div class="flex justify-between gap-5 h-[193px]">
          <p class="text-base font-medium w-[400px] xl:w-[450px]">
            Tab Setting Disabled
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  setup() {
    const openTab = ref(1);

    const toggleTabs = (tabNumber) => {
      openTab.value = tabNumber;
    };

    return {
      openTab,
      toggleTabs,
    };
  },
};
</script>

<style></style>
