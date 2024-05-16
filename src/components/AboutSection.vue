<template>
    <div class="bg-white">
      <div class="container mx-auto px-4">
        <div class="grid grid-cols-12 gap-4 py-4">
          <div class="col-span-12 lg:col-span-6 md:col-span-6 sm:col-span-12">
            <p class="text-2xl text-[#29275b] font-bold">{{ styleAndAdvice.title }}</p>
            <h1 class="py-8 text-[#59595b] font-bold text-4xl">{{ styleAndAdvice.subtitle }}</h1>
            <p class="text-lg leading-7 text-[#59595b] font-medium">{{ styleAndAdvice.description }}</p>
            <button class="py-4 bg-[#29275b] text-center font-bold leading-4 text-sm px-12 rounded text-white my-10 uppercase">Watch The Videos</button>
          </div>
          <div class="col-span-12 lg:col-span-6 md:col-span-6 sm:col-span-12">
            <img :src="styleAndAdvice.image" :alt="styleAndAdvice.title">
          </div>
        </div>
        <div class="grid grid-cols-12 gap-2 lg:gap-8 py-4 items-center">
          <div class="col-span-12 lg:col-span-3 md:col-span-6 sm:col-span-12 items-center">
            <p class="text-3xl font-bold text-[#29275b]">{{ customerReview.title }}</p>
          </div>
          <div class="col-span-12 lg:col-span-3 md:col-span-6 sm:col-span-12">
            <img :src="customerReview.starsImage" :alt="customerReview.title" class="max-w-full h-12">
          </div>
          <div class="col-span-12 lg:col-span-3 md:col-span-6 sm:col-span-12">
            <p class="text-2xl font-bold text-[#29275b]">{{ customerReview.rating }}</p>
          </div>
          <div class="col-span-12 lg:col-span-3 md:col-span-6 sm:col-span-12">
            <img :src="customerReview.trustpilotLogo" :alt="customerReview.title" class="max-w-full h-12">
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  import videoimage from  "@/assets/video image.jpg";
  import stars from  "@/assets/stars.svg";
  import trustLogo from  "@/assets/trustpilot-logo.svg";
  export default {
    data() {
      return {
        styleAndAdvice: {
          title: 'Style & Advice:',
          subtitle: 'Tiling tips with Craig Phillips',
          description: 'As one of the UK’s leading DIY and home improvement TV experts, Craig Phillips is the perfect person to bring you our series of ‘How To’ videos. These handy tutorials are designed to answer your most frequently asked questions about tiling.',
          image: videoimage
        },
        customerReview: {
          title: 'Our customers love us!',
          starsImage: stars,
          rating: '4.6 out of 5 - Rated Excellent!',
          trustpilotLogo: trustLogo
        }
      };
    }
  };
  </script>
  