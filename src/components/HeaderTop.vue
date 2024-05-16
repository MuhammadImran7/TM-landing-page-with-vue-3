
<template>
  <div class="container mx-auto">
    <div class="grid grid-cols-12 gap-4 items-center px-4">
          <div class="col-span-6 lg:col-span-2 md:col-span-6 sm:col-span-12">
            <img :src="imageUrl" alt="">
          </div>
          <div class="col-span-12 lg:col-span-4 md:col-span-6 sm:col-span-12">
            <input type="text" 
            class="bg-[#e5ebee] border border-gray-300 focus:border-green-500 outline-none px-4 py-2 placeholder-gray-400 w-full lg:w-3/4"
            placeholder="What are you looking for">
          </div>
          <div class="col-span-6 lg:col-span-2 md:col-span-6 sm:col-span-12">
            <div class="flex gap-2 items-center">
                <!-- <i class="fa-brands fa-rocketchat text-2xl"></i> -->
                <img :src="chatlogo" alt="" class="h-5 w-6">
                <p class="font-bold text-base text-[#29275b] ml-1">Need help?</p>
            </div>
          </div>
          <div class="col-span-12 lg:col-span-4 md:col-span-6 sm:col-span-12">
            <div class="flex gap-10 items-center lg:justify-center md:justify-start sm:justify-start">
                <div class="pt-6">
                    <img :src="location" alt="" class="h-5 w-6">
                    <p>Showrooms</p>
                </div>
                <img :src="user" alt="" class="h-5 w-6">
                <img :src="basket" alt="" class="h-5 w-6">
            </div>
          </div>
        </div>
  </div>
</template>
<script>
// Import the image using a relative path
import logo from '/src/assets/logo.svg'; // Assuming the image is located in the assets directory
import chatlogo from '/src/assets/chatlogo (1).svg'; // Assuming the image is located in the assets directory
import location from '/src/assets/location.svg';
import user from '/src/assets/user.svg';
import basket from '/src/assets/basket.svg';

export default {
  data() {
    return {
      imageUrl: logo, chatlogo, location, user, basket, // Assign the imported image to a variable
    };
  },
};
</script>

<style>

</style>
