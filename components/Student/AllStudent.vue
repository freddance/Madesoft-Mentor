<template>
  <diiv class="grid grid-cols-4 " style="padding: 26px 0px 0px 0px;">
    <div class="px-4 py-6 student-card">
      <div class="flex justify-between">
        <div class="card-active text-center pt-1">
          Active
        </div>

        <div class="flex justify-end ml-auto">
          <Menu as="div" class="relative ml-3 lg:mr-0 mr-8">
            <div>
              <MenuButton class="flex">
                <svg xmlns="http://www.w3.org/2000/svg" width="4" height="18" viewBox="0 0 4 18" fill="none">
                  <rect width="4" height="3.6" fill="#101010"/>
                  <rect y="7.2002" width="4" height="3.6" fill="#101010"/>
                  <rect y="14.3999" width="4" height="3.6" fill="#101010"/>
                </svg>
              </MenuButton>
            </div>
            <transition enter-active-class="transition ease-out duration-100" enter-from-class="transform opacity-0 scale-95" enter-to-class="transform opacity-100 scale-100" leave-active-class="transition ease-in duration-75" leave-from-class="transform opacity-100 scale-100" leave-to-class="transform opacity-0 scale-95">
              <MenuItems class="absolute right-0 z-10 mt-2 w-48 origin-top-right rounded-md bg-white py-1 shadow-lg  ring-opacity-5 focus:outline-none">
                <MenuItem v-slot="{ active }">
                  <nuxt-link to="/student/profile" :class="[active ? 'bg-gray-100' : '', 'block px-4 py-2 text-sm text-gray-700']">View Profile</nuxt-link>
                </MenuItem>
                <MenuItem>
                  <h6 class="'block px-4 py-2 text-sm text-gray-700'">Feedback</h6>
                </MenuItem>
                <MenuItem v-slot="{ active }">

                  <a  :class="[active ? 'bg-gray-100' : '', 'block px-4 py-2 text-sm text-gray-700']">Delete</a>
                </MenuItem>
              </MenuItems>
            </transition>
          </Menu>
        </div>

        <div class="pt-0.5">

        </div>
      </div>

      <div class="gap-16 flex justify-center pt-4">
        <img src="~assets/images/MaskGroup.svg" alt="" srcset="">
      </div>

      <div class="text-center pt-4">
        <h2 class="text-lg font-medium">Christian Okpara</h2>
        <p>User ID: 423AGhN</p>
        <p>+2348012345768</p>
        <p class="border-b pb-6">sharonaceemeruwa@gmail.com</p>
      </div>

      <div class="card_ text-center pt-1 pb-1 mt-4 mx-4">
        Program: Mechanical
      </div>
    </div>
  </diiv>
</template>

<script setup>
import {  Menu, MenuButton, MenuItem, MenuItems } from '@headlessui/vue'
</script>

<style scoped>
.student-card {
  box-shadow: 0px 4px 10px 0px rgba(0, 0, 0, 0.10);
  border-radius: 10px;
  background: #FFF;
}

.card-active{
  border-radius: 20px;
  background: var(--success-green-50, #ECFDF5);
  color: var(--Natural-Accent, #059669);
  font-size: 11px;
  width: 64px;
  height: 26px;

}

.card_ {
  border-radius: 8px;
  background: #F3F7FF;
}
</style>