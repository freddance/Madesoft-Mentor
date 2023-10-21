<template>
  <div>

    <div class="bg-white px-10 py-6">
      <h1 class="font-bold head-text">Assignment Status</h1>
    </div>

    <div class="flex px-10 mt-8 mb-4">
      <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
        <path d="M10.875 19.3L4.27502 12.7C4.17502 12.6 4.10402 12.4917 4.06202 12.375C4.02002 12.2583 3.99935 12.1333 4.00002 12C4.00002 11.8667 4.02102 11.7417 4.06302 11.625C4.10502 11.5083 4.17568 11.4 4.27502 11.3L10.875 4.7C11.0583 4.51667 11.2877 4.421 11.563 4.413C11.8383 4.405 12.0757 4.50067 12.275 4.7C12.475 4.88333 12.5793 5.11267 12.588 5.388C12.5967 5.66333 12.5007 5.90067 12.3 6.1L7.40002 11H18.575C18.8583 11 19.096 11.096 19.288 11.288C19.48 11.48 19.5757 11.7173 19.575 12C19.575 12.2833 19.4793 12.521 19.288 12.713C19.0967 12.905 18.859 13.0007 18.575 13H7.40002L12.3 17.9C12.4833 18.0833 12.5793 18.3167 12.588 18.6C12.5967 18.8833 12.5007 19.1167 12.3 19.3C12.1167 19.5 11.8833 19.6 11.6 19.6C11.3167 19.6 11.075 19.5 10.875 19.3Z" fill="#FF4155"/>
      </svg>
      <span style="color: #FF4155;">Back</span>
    </div>

    <div class="px-10 mt-8">
      <div class="overview-card py-3">
        <div class="flex justify-between">
          <div>
            <div  class="flex gap-x-6 mx-4 mt-2 px-4">
              <div class="cursor-pointer " @click="toggleType(OPTION_1)" :class="[type === OPTION_1 ? 'active pb-2' : '']">All Submissions</div>
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
      </div>
    </div>

    <div class="px-10 mt-16">
      <div v-if="type === OPTION_1" class="mt-8">
        <div class="relative overflow-x-auto shadow-sm sm:rounded-lg mt-6">
          <table class="w-full text-sm  space text-left text-gray-500 dark:text-gray-400">
            <thead class="text-xs uppercase table-head ">
            <tr>
              <th scope="col" class="px-6 py-5">

              </th>
              <th scope="col" class="px-6 py-5">
                S/N
              </th>
              <th scope="col" class="px-6 py-5 whitespace-nowrap">
                Student Name
              </th>
              <th scope="col" class="px-6 py-5">
                Assignment
              </th>
              <th scope="col" class="px-6 py-5">
                Date Submitted
              </th>
              <th scope="col" class="px-6 py-3  whitespace-nowrap">
                Status
              </th>
            </tr>
            </thead>

            <tbody class="">
            <tr class="bg-white " style="border-bottom: 0.8px solid var(--gray-200, #EAECF0);">

              <td class="px-6 py-6">
                <Menu as="div" class="relative">
                  <div>
                    <MenuButton class="flex gap-4">
                      <button class="w-full ">
                        <svg xmlns="http://www.w3.org/2000/svg" width="4" height="18" viewBox="0 0 4 18" fill="none">
                          <rect width="4" height="3.6" fill="#101010"/>
                          <rect y="7.2002" width="4" height="3.6" fill="#101010"/>
                          <rect y="14.3999" width="4" height="3.6" fill="#101010"/>
                        </svg>
                      </button>

                    </MenuButton>
                  </div>
                  <transition enter-active-class="transition ease-out duration-100" enter-from-class="transform opacity-0 scale-95" enter-to-class="transform opacity-100 scale-100" leave-active-class="transition ease-in duration-75" leave-from-class="transform opacity-100 scale-100" leave-to-class="transform opacity-0 scale-95">
                    <MenuItems class="absolute left-0 z-10 mt-2 w-48 origin-top-right rounded-md bg-white py-1 shadow-lg  ring-opacity-5 focus:outline-none">
                      <MenuItem v-slot="{ active }" style="background: #FFEAEC; color: #FF4155;" >
                        <nuxt-link to="/my-program/view-submission" :class="[active ? 'bg-gray-100' : '', 'block px-4 py-2 text-sm text-gray-700 cursor-pointer']">View Assignment Status</nuxt-link>
                      </MenuItem>
                      <MenuItem>
                        <h6 :class="[active ? 'bg-gray-100' : '', 'block px-4 py-2 text-sm text-gray-700 cursor-pointer']">Download</h6>
                      </MenuItem>
                    </MenuItems>
                  </transition>
                </Menu>
              </td>

              <td class="px-6 py-6">
                1
              </td>

              <td class="px-6 py-6">
                Austine Jonah
              </td>

              <td class="px-6 py-6">
                SAE - Assignment
              </td>

              <td class="px-6 py-6">
                2 months ago
              </td>

              <td class="px-6 py-6">
                <div class="p-2 text-center " style="background: rgba(0, 234, 51, 0.05); border-radius: 20px; color: #00EA33;">
                  Checked
                </div>
              </td>
            </tr>

            </tbody>
          </table>

        </div>
      </div>

    </div>

  </div>
</template>


<script setup>
import {useQueryParamsTabSwitch} from "~/composables/useSwitchQueryParams";
import Assignment from "~/components/MyProgram/Assignment.vue";
import GradeBook from "~/components/MyProgram/GradeBook.vue";
import Syllables from "~/components/MyProgram/Syllables.vue";
import {Menu, MenuButton, MenuItem, MenuItems} from "@headlessui/vue";

let tabs = [
  'Modules',

]

const type = useQueryParamsTabSwitch(tabs);
const OPTION_1 = tabs[0];

const toggleType = (_type) => {
  type.value = _type
}
</script>

<style scoped>
.overview-card {
  border-radius: 10px 10px 0px 0px;
  background: var(--White, #FFF);
  box-shadow: 0px 4px 10px 0px rgba(0, 0, 0, 0.08);
}

.active {
  border-bottom: 2px solid #FF4155;;
}
</style>