<template>
    <div class="bg-[#f1f1f1] mt-2">
      <div class="container mx-auto px-4">
        <div class="grid grid-cols-12 gap-4 py-4">
          <!-- Use v-for to generate items -->
          <div v-for="(item, index) in items" :key="index" :class="`col-span-12 lg:col-span-4 md:col-span-6 sm:col-span-12`">
            <div class="flex justify-evenly">
              <div class="flex items-center">
                <!-- Use dynamic icons -->
                <img :src="item.icon" alt="" class="h-8 w-8">
                <!-- Use dynamic text -->
                <p class="font-bold text-base text-[#29275b] ml-3">{{ item.text }}</p>
              </div>
            </div>
          </div>
        </div>
        <div class="grid grid-cols-12 gap-4 py-4 text-center place-content-center">
        <div v-for="(product, index) in products" :key="index" class="col-span-12 lg:col-span-4 md:col-span-6 sm:col-span-12">
          <div class="relative">
            <img :src="product.image" :alt="product.title" class="w-full">
            <div class="bg-gray-400 bg-opacity-40 text-center absolute bottom-0 w-full">
              <h3 class="font-bold text-[#29275b] py-6 px-6 text-xl">{{ product.title }}</h3>
            </div>
          </div>
        </div>
      </div>
      </div>
    </div>
  </template>
  
  <script>
  import truck from "@/assets/truck.png";
  import user from "@/assets/user.svg";
  import star from "@/assets/star.png";
  import outdoorPavingSlabs from "@/assets/r-outdoorslabs.jpg";
  import bathroomtiles from "@/assets/r-bathroom.jpg";
  import flooring from "@/assets/r-flooring.jpg";
  import laminateflooring from "@/assets/r-laminateflooring.jpg";
  import realwood from "@/assets/r-realwood.jpg";
  import vinyl from "@/assets/r-vinyl.jpg";
  import woodeffect from "@/assets/r-woodeffect.jpg";
  import stylishSaving from "@/assets/stylish-savings-407.jpg";
  
  export default {
    data() {
      return {
        // Define items with dynamic text and icon classes
        items: [
          { text: "Fast, Free Delivery Over £299*", icon: truck },
          { text: "Fast, Free Delivery Over £290*", icon: user },
          { text: "Fast, Free Delivery Over £289*", icon: star }
        ],
        products: [
            { title: "Outdoor Paving Slabs", image: outdoorPavingSlabs },
            { title: "Bathroom Tiles", image: bathroomtiles },
            { title: "Flooring", image: flooring },
            { title: "Laminate Flooring", image: laminateflooring },
            { title: "Outdoor Slabs", image: outdoorPavingSlabs },
            { title: "Real Wood", image: realwood  },
            { title: "Vinyl Flooring", image: vinyl },
            { title: "Wood Effect", image: woodeffect },
            { title: "Stylish Savings", image: stylishSaving }
        ]
      };
    }
  };
  </script>
  