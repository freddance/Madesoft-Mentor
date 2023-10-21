<template>
  <div>
    <div class="bg-white px-10 py-4 pb-8">
      <div class="flex">
        <h1 class="font-semibold head-text">Welcome back!</h1> <h1 class="head-text ml-2">Olu.</h1>
      </div>
      <p style="color: #8A8C8D;">27 August 2023</p>
    </div>


    <div class="mt-8 mx-10 pt-4 bg-white pb-8" style="border-radius: 8px;">

      <div class="grid lg:grid-cols-4 gap-5 px-4 p-3 pb-5 mt-2">
        <div class="overview-card-inner p-4  justify-between ">
          <div class="">
            <span class="sub-head font-extralight text-md">Total Courses</span>
            <h2 class="font-extrabold text-xl pt-2">346</h2>
          </div>

          <div>
            <div class="flex">
              <div class="pt-6">
                <svg xmlns="http://www.w3.org/2000/svg" width="104" height="19" viewBox="0 0 104 19" fill="none">
                  <path opacity="0.3" d="M0 13H28.5L40 4.5L36.5 17L52.5 4.5L49.5 17L63.5 2V13H103.5" stroke="#FF4155"/>
                </svg>
              </div>

              <div class="flex justify-end ml-auto">
                <img src="~assets/images/Group62.svg" class="pt-2" alt="">
              </div>
            </div>
          </div>
        </div>

        <div class="overview-card-inner p-4  justify-between ">
          <div class="">
            <span class="sub-head font-extralight text-md">Total Students</span>
            <h2 class="font-extrabold text-xl pt-2">100</h2>
          </div>

          <div>
            <div class="flex">
              <div class="pt-6">
                <svg xmlns="http://www.w3.org/2000/svg" width="104" height="19" viewBox="0 0 104 19" fill="none">
                  <path opacity="0.3" d="M0 13H28.5L40 4.5L36.5 17L52.5 4.5L49.5 17L63.5 2V13H103.5" stroke="#6D4C41"/>
                </svg>
              </div>

              <div class="flex justify-end ml-auto">
                <img src="~assets/images/Group63.svg" class="pt-2" alt="">
              </div>
            </div>
          </div>
        </div>


        <div class="overview-card-inner p-4  justify-between ">
          <div class="">
            <span class="sub-head font-extralight text-md">Total Revenue</span>
            <h2 class="font-extrabold text-xl pt-2">N4,000,000</h2>
          </div>

          <div>
            <div class="flex">
              <div class="pt-6">
                <svg xmlns="http://www.w3.org/2000/svg" width="104" height="19" viewBox="0 0 104 19" fill="none">
                  <path opacity="0.3" d="M0 13H28.5L40 4.5L36.5 17L52.5 4.5L49.5 17L63.5 2V13H103.5" stroke="#0DE337"/>
                </svg>
              </div>

              <div class="flex justify-end ml-auto">
                <img src="~assets/images/Group64.svg" class="pt-2" alt="">
              </div>
            </div>
          </div>
        </div>


      </div>


      <div class="mt-6 p-4 grid grid-cols-5 gap-x-6">
        <div class="col-span-2 mt-2">
          <div class="attendance p-4">
            <div class="flex justify-between">
              <div class="">
                <h1 class="text-lg font-medium">Feedback Activity</h1>
                <span>5h 45min</span>
              </div>
              <div>
                <Dropdown v-model="selectedCity" :options="cities" optionLabel="name" placeholder="Students" class="w-full md:w-14rem" />
              </div>
            </div>

            <div>

            </div>
          </div>
        </div>


        <div class="col-span-2">
          <h1 class="font-medium text-lg">Upcoming Class</h1>
          <div class="attendance flex p-4 mt-4">
            <div class="time">
              9:00 am
            </div>
            <div class="text-sm ml-4">
              <h1>Introduction Industrial Automation</h1>
              <p style="color: #8A8C8D;" class="pt-1">Online <span class="ml-6">-</span>  <span class="ml-8"> Google meet</span></p>
            </div>
          </div>

          <div class="attendance flex p-4 mt-6">
            <div class="time">
              9:00 am
            </div>
            <div class="text-sm ml-4">
              <h1>Introduction Industrial Automation</h1>
              <p style="color: #8A8C8D;" class="pt-1">Online <span class="ml-6">-</span>  <span class="ml-8"> Google meet</span></p>
            </div>
          </div>
        </div>

        <div class="mt-4">
          <img src="~assets/images/back-to-programs.svg" alt="">
        </div>
      </div>


      <div class="p-4 mt-4">
        <div class="Schedule-class text-center text-lg font-medium">
          Schedule a Class
        </div>
      </div>


    </div>
  </div>
</template>

<script setup>
</script>

<style scoped>
.overview-card-inner {
  border-radius: 4px;
  background: var(--shades-white, #FFF);
  box-shadow: 0px 4px 10px 0px rgba(0, 0, 0, 0.10);
}

.attendance {
  border-radius: 8px;
  background: var(--White, #FFF);
  box-shadow: 0px 0.4px 2px 0px rgba(16, 24, 40, 0.06), 0px 0.5px 3px 0px rgba(16, 24, 40, 0.10);
}

span{
  color: #626466;
  font-size: 14px;
}

.time {
  border-radius: 4px;
  background: #FFF;
  box-shadow: 0px 3px 6px 0px rgba(0, 0, 0, 0.09);
  padding: 11px 8px 12px 8px;
}

.Schedule-class {
  background: #FFF;
  box-shadow: 0px 2px 9px 4px rgba(0, 0, 0, 0.04);
  color: #FF4155;
  padding: 23px 474px 23px 402px;
}
</style>