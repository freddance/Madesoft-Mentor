<template>
  <div>

    <h1 class="font-bold text-lg mt-8">Assignments</h1>
  </div>

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
          Assignment Title
        </th>
        <th scope="col" class="px-6 py-5">
          Module
        </th>
        <th scope="col" class="px-6 py-5">
          Lesson
        </th>
        <th scope="col" class="px-6 py-5">
          Date
        </th>
        <th scope="col" class="px-6 py-3  whitespace-nowrap">
          Total Submission
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
                  <nuxt-link to="/my-program/view-assignment" :class="[active ? 'bg-gray-100' : '', 'block px-4 py-2 text-sm text-gray-700 cursor-pointer']">View Assignment Status</nuxt-link>
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
          SAE - Assignment
        </td>

        <td class="px-6 py-6">
          Fundamentals Of Industrial Automation
        </td>

        <td class="px-6 py-6">
          Lesson 3 – Equipment’s Used In Industrial Automation
        </td>

        <td class="px-6 py-6">
          20/6/2023
        </td>
        <td class="px-6 py-6">
          <div class="p-2 text-center text-white" style="background: #130204; border-radius: 20px;">
            50
          </div>
        </td>
      </tr>

      </tbody>
    </table>

  </div>
</template>

<script setup>
import {  Menu, MenuButton, MenuItem, MenuItems } from '@headlessui/vue'
import { ref, onMounted } from 'vue';

const OptionsModal = ref(false)


const customers = ref([
  {
    id: 1,
    name: 'James Butt',
    country: {
      name: 'Algeria',
      code: 'dz'
    },
    company: 'Benton, John B Jr',
    date: '2015-09-13',
    status: 'completed',
    verified: true,
    activity: 17,
    representative: {
      name: 'Ioni Bowcher',
      image: 'ionibowcher.png'
    },
    balance: 70663
  },

]);

</script>


<style scoped>



.completed {
  border-radius: 20px;
  background: var(--success-50, #ECFDF3);
  color: var(--success-500, #12B76A);
  padding: 8px 19px;
  width: 107px;
}

.Incomplete {
  border-radius: 20px;
  background: var(--warning-50, #FFFAEB);
  color: var(--warning-500, #F79009);
  padding: 8px 19px;
  width: 107px;

}
</style>