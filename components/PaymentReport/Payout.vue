<template>
  <div>
    <div class="grid grid-cols-4 mt-8 gap-x-6">
      <div class="p-5 total-payout text-white">
        <div class="font-light">Total Payout</div>
        <div class="font-semibold pt-3 text-xl">
          N400,000
        </div>

        <div class="flex justify-end ml-auto">
          <img src="~assets/images/Group626800.svg" alt="" srcset="">
        </div>
      </div>

      <div class="p-5 pending text-white">
        <div class="font-light">Pending Payout</div>
        <div class="font-semibold pt-3 text-xl">
          N112,000
        </div>

        <div class="flex justify-end ml-auto">
          <img src="~assets/images/Group626800.svg" alt="" srcset="">
        </div>
      </div>

      <div class="p-5 canceled text-white">
        <div class="font-light">Cancelled Payout</div>
        <div class="font-semibold pt-3 text-xl">
          N50,000
        </div>

        <div class="flex justify-end ml-auto">
          <img src="~assets/images/Group626800.svg" alt="" srcset="">
        </div>
      </div>

      <div class="p-5 requested text-white">
        <div class="font-light">Requested Payout</div>
        <div class="font-semibold pt-3 text-xl">
          6
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
</template>

<style scoped>
.total-payout {
  border-radius: 4px;
  background: #008D99;
  box-shadow: 0px 4px 10px 0px rgba(0, 0, 0, 0.10);
}

.pending {
  border-radius: 4px;
  background: #CD3C17;
  box-shadow: 0px 4px 10px 0px rgba(0, 0, 0, 0.10);
}

.canceled {
  border-radius: 4px;
  background: #373737;
  box-shadow: 0px 4px 10px 0px rgba(0, 0, 0, 0.10);
}

.requested {
  border-radius: 4px;
  background: #C31162;
  box-shadow: 0px 4px 10px 0px rgba(0, 0, 0, 0.10);
}
</style>