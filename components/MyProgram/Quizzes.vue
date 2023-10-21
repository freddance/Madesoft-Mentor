<template>
  <div>

    <div class="px-10 mt-16">
      <div class="mt-8">
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
                Quiz Title
              </th>
              <th scope="col" class="px-6 py-5">
                Module
              </th>
              <th scope="col" class="px-6 py-5">
                Topic
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
                        <nuxt-link to="/my-program/view-quiz" :class="[active ? 'bg-gray-100' : '', 'block px-4 py-2 text-sm text-gray-700 cursor-pointer']">View Quiz</nuxt-link>
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
                SAE - Quiz
              </td>

              <td class="px-6 py-6">
                Fundamentals Of Industrial Automation
              </td>

              <td class="px-6 py-6">
                Topic 1 – Equipment’s Used In Industrial Automation
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