<template>
    <div>
      <div class="bg-white px-10 py-4">
          <h1 class="font-semibold head-text">My Programs</h1>
        </div>


       <div class="px-10">
        <div class="grid grid-cols-1 mt-12 bg-white py-10 px-6" style="border-radius: 8px;" >
            <div class="flex flex-row program-card p-6 gap-10">
                <div>
                    <img src="~assets/images/SE.svg" alt="" srcset="">
                </div>

                <div>
                    <h1 class="font-medium text-2xl">MAT CIAPP - Certificate in Industrial Automation and PLC Programming</h1>

                    <div class="flex gap-8 mt-5 border-b pb-4" style="">
                        <div style="border-radius: 100px; background: #F9F9F9; padding: 10px 12px; ">
                            Electrical Engineering
                        </div>
                        <div class="pt-2.5 font-light"  style="color: #FF4155;">
                            23 Lessons
                        </div>
                        <div class="pt-2.5 font-light" style="color: #FF4155;">
                            2 Assignments
                        </div>
                        <div class="pt-2.5 font-light"  style="color: #FF4155;">
                            1 Project
                        </div>
                    </div>

                    <div class="grid grid-cols-3">
                        <div class="col-span-2 pt-4">
                          <div style="color: #7C7C7C;" class="text-sm">
                            Start Date: 14 July 2023
                          </div>
                        </div>
                       <div class="mt-4">
                         <nuxt-link to="/my-program/view-program" class="bg-black text-white flex justify-end ml-auto" style="padding: 18px 25px; border-radius: 100px; width: 156px;">
                           View Program
                         </nuxt-link>
                       </div>
                    </div>
                </div>
            </div>

            <div class="text-center mt-10 " style="color: #FF4155; text-decoration-line: underline;">
                Add More Programs
            </div>
        </div>
       </div>
  
      
    </div>
  </template>
  
  <script setup>
  </script>
  
  <style scoped>
  .program-card {
    border-radius: 20px;
    border: 1px solid #FAFAFA;
    background: rgba(247, 252, 255, 0.30);
    box-shadow: 0px 6px 9px 0px rgba(0, 0, 0, 0.10);
  }

  .button {}
  </style>