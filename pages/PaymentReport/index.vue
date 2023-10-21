<template>
  <div>

    <div class="bg-white px-12 py-6">
      <h1 class="font-bold head-text">Assignment Status</h1>
    </div>


    <div class="px-12 mt-8">
      <div class="overview-card py-3">
        <div class="flex justify-between">
          <div>
            <div  class="flex gap-x-6 mx-4 mt-2 px-4">
              <div class="cursor-pointer " @click="toggleType(OPTION_1)" :class="[type === OPTION_1 ? 'active pb-2' : '']">Revenue</div>
              <div class="cursor-pointer " @click="toggleType(OPTION_2)" :class="[type === OPTION_2 ? 'active pb-2' : '']">Payout</div>
              <div class="cursor-pointer " @click="toggleType(OPTION_3)" :class="[type === OPTION_3 ? 'active pb-2' : '']">Reviews</div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="px-12 mt-10">
      <div v-if="type === OPTION_1" class="mt-8">
        <div class="grid grid-cols-4 mt-8 gap-x-6">
          <div class="p-5 total-rev text-white">
            <div class="font-light">Total  Revenue</div>
            <div class="font-semibold pt-3 text-xl">
              N1,000,000
            </div>

            <div class="flex justify-end ml-auto">
              <img src="~assets/images/Group626800.svg" alt="" srcset="">
            </div>
          </div>
            <div class="p-5 total-paid text-white">
            <div class="font-light">Total Paid Revenue</div>
            <div class="font-semibold pt-3 text-xl">
              N300,000
            </div>

            <div class="flex justify-end ml-auto">
              <img src="~assets/images/Group626800.svg" alt="" srcset="">
            </div>
          </div>

          <div class="p-5 total-unpaid text-white">
            <div class="font-light">Total UnPaid Revenue</div>
            <div class="font-semibold pt-3 text-xl">
              N350,000
            </div>

            <div class="flex justify-end ml-auto">
              <img src="~assets/images/Group626800.svg" alt="" srcset="">
            </div>
          </div>

          <div class="p-5 total-req text-white">
            <div class="font-light">Total UnPaid Revenue</div>
            <div class="font-semibold pt-3 text-xl">
              N350,000
            </div>

            <div class="flex justify-end ml-auto">
              <img src="~assets/images/Group626800.svg" alt="" srcset="">
            </div>
          </div>
        </div>

        <h1 class="font-medium text-lg mt-12">Revenue History</h1>
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
        <Payout />
      </div>

      <div  v-if="type === OPTION_3">
        <Review />
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
import Payout from "~/components/PaymentReport/Payout.vue";
import Review from "~/components/PaymentReport/Review.vue";

let tabs = [
  'Revenue',
  'payout',
  'Reviews',

]

const type = useQueryParamsTabSwitch(tabs);
const OPTION_1 = tabs[0];
const OPTION_2 = tabs[1];
const OPTION_3 = tabs[3];

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


.total-rev{
  border-radius: 4px;
  background: #5F0467;
  box-shadow: 0px 4px 10px 0px rgba(0, 0, 0, 0.10);
}

.total-paid {
  border-radius: 4px;
  background: #064814;
  box-shadow: 0px 4px 10px 0px rgba(0, 0, 0, 0.10);
}

.total-unpaid {
  border-radius: 4px;
  background: #584143;
  box-shadow: 0px 4px 10px 0px rgba(0, 0, 0, 0.10);
}

.total-req {
  border-radius: 4px;
  background: #6F5D00;
  box-shadow: 0px 4px 10px 0px rgba(0, 0, 0, 0.10);
}
</style>