<template>
  <div>
    <div class="max-w-5xl mx-auto py-10">
      <h1 class="text-4xl font-semibold mx-4 my-10">What Our Customers Say</h1>
      <!-- <ul class="flex flex-wrap justify-center">
      <li
        v-for="review in ebayFeedback"
        :key="review.review"
        class="w-3/12 p-4 border-gray-400 bg-white rounded-xl m-4 flex flex-wrap shadow"
      >
        <div class="w-full">
          <p class="text-lg font">{{ review.review }}</p>
        </div>
        <div class="w-full text-right self-end mt-4">
          <p class="">{{ review.userName }}</p>
        </div>
      </li>
    </ul> -->
      <!--  -->
      <div class="flex flex-wrap justify-center">
        <div
          class="w-full mx-auto rounded-lg bg-white border border-gray-200 p-5 text-gray-800 font-light mb-6 max-w-xs"
          v-for="review in ebayFeedback"
          :key="review.review"
        >
          <div class="w-full flex mb-4 items-center">
            <!-- <div
          class="overflow-hidden rounded-full w-10 h-10 bg-gray-50 border border-gray-200"
        >
          <img src="https://i.pravatar.cc/100?img=1" alt="" />
        </div> -->
            <div class="flex-grow pl-3">
              <h6 class="font-bold text-sm uppercase text-gray-600">
                {{ review.userName }}
              </h6>
            </div>
          </div>
          <div class="w-full">
            <p class="text-sm leading-tight">
              <span
                class="text-lg leading-none italic font-bold text-gray-400 mr-1"
                >"</span
              >{{ review.review
              }}<span
                class="text-lg leading-none italic font-bold text-gray-400 ml-1"
                >"</span
              >
            </p>
          </div>
        </div>
        <!--  -->
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  data() {
    const ebayFeedback = require('@/assets/ebayFeedback.json').root
    return { ebayFeedback }
  },
})
</script>

