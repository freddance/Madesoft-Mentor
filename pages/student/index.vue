<template>
  <div>

    <div class="bg-white px-10 py-6">
      <h1 class="font-bold head-text">Student</h1>
    </div>

    <div class="px-10 mt-5">
      <div class="overview-card py-4">
        <div class="flex justify-between pb-2">
          <div style="background: #FBFCFF; padding: 6px 12px;" class=" gap-x-6 mx-4">
            <div class="flex gap-x-6 pt-2">
              <div class="cursor-pointer px-2" @click="toggleType(OPTION_1)" :class="[type === OPTION_1 ? 'active' : '']">Overview</div>
              <div class="cursor-pointer px-2" @click="toggleType(OPTION_2)" :class="[type === OPTION_2 ? 'active' : '']">All Student</div>
            </div>
          </div>

          <div class="px-6">
            <div class="relative">
              <div class="absolute inset-y-0 left-0 flex items-center pl-3 bottom-5 md:bottom-0 pointer-events-none">
                <svg aria-hidden="true" class="w-5 h-5 text-gray-500 dark:text-gray-400" fill="none" stroke="currentColor"
                     viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"></path>
                </svg>
              </div>
              <div class="flex">
                <div class="">
                  <input v-model="search" type="search" id="default-search"
                         class="block input p-4 pl-10  md:w-[200px]  text-sm text-gray-900 rounded-[5px]  bg-white focus:ring-none outline-none  dark:placeholder-black dark:text-black dark:focus:ring-blue-500 "
                         placeholder="Search " required>
                </div>
              </div>


            </div>
          </div>
        </div>

        <div v-if="type === OPTION_1" class="border-t">
          <OverViewCard />
        </div>

        <div v-if="type === OPTION_2">

        </div>


      </div>

      <div  v-if="type === OPTION_1">
        <div>

          <h1 class="font-medium text-lg mt-12">Student History</h1>
        </div>

        <div class="relative overflow-x-auto shadow-sm sm:rounded-lg mt-4">
          <table class="w-full text-sm  space text-left text-gray-500 dark:text-gray-400">
            <thead class="text-xs uppercase table-head ">
            <tr>
              <th scope="col" class="px-6 py-5">
                S/N
              </th>
              <th scope="col" class="px-6 py-5  whitespace-nowrap">
                Full Name
              </th>
              <th scope="col" class="px-6 py-5">
                Email
              </th>
              <th scope="col" class="px-6 py-5 whitespace-nowrap">
                Phone Number
              </th>
              <th scope="col" class="px-6 py-5">
                Program
              </th>
              <th scope="col" class="px-6 py-5  whitespace-nowrap">
                Payment Status
              </th>
              <th scope="col" class="px-6 py-5  whitespace-nowrap">
                Date Joined
              </th>
              <th scope="col" class="px-6 py-3  whitespace-nowrap">
                Details
              </th>
            </tr>
            </thead>

            <tbody class="">
            <tr class="bg-white " style="border-bottom: 0.8px solid var(--gray-200, #EAECF0);">

              <td class="px-6 py-6">
                1
              </td>

              <td class="px-6 py-6">
                David Adetoyi
              </td>

              <td class="px-6 py-6">
                davidadetoyi@gmail.com
              </td>

              <td class="px-6 py-6">
                07031945084
              </td>

              <td class="px-6 py-6">
                MAT CFWDP - Certificate In Frontend Web Development
              </td>

              <td class="px-6 py-6">
                <div class="p-2 text-center text-white" style="background: #ECFDF3; color: #12B76A; border-radius: 20px;">
                  Completed
                </div>
              </td>
              <td class="px-6 py-6">
                20/6/2023
              </td>

              <td class="px-6 py-6" style="color: #FF4155;">
                <nuxt-link to="/Student/Profile">View</nuxt-link>
              </td>
            </tr>

            </tbody>
          </table>

        </div>
      </div>

      <div  v-if="type === OPTION_2">
        <StudentAllStudent />
      </div>


    </div>
  </div>
</template>


<script setup>
import {useQueryParamsTabSwitch} from "~/composables/useSwitchQueryParams";
import OverViewCard from "~/components/Student/OverViewCard.vue";
import {Menu, MenuButton, MenuItem, MenuItems} from "@headlessui/vue";

let tabs = [
  'Overview',
  'All student',
]

const type = useQueryParamsTabSwitch(tabs);
const OPTION_1 = tabs[0];
const OPTION_2 = tabs[1];

const toggleType = (_type) => {
  type.value = _type
}
</script>

<style scoped>
.overview-card {
  border-radius: 8px;
  border: 1px solid var(--light-border, #EAECF0);
  background: var(--White, #FFF);
  box-shadow: 0px 0.4px 2px 0px rgba(16, 24, 40, 0.06), 0px 0.5px 3px 0px rgba(16, 24, 40, 0.10);
}

.active {
  color: #FF4155;
  border-radius: 4px;
  font-weight: 600;
  border: 1px solid #F8F8F8;
  background: var(--shades-white, #FFF);
  box-shadow: 0px 9px 6px -7px rgba(0, 0, 0, 0.09), 0px 0px 0px -1px rgba(0, 0, 0, 0.25);
}
</style>