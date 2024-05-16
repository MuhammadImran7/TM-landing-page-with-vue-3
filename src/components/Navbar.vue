
<template>
  <div class="bg-[#24224d]">
    <div class="container mx-auto">
      <nav class="w-full mt-2">
        <ul class="flex justify-around flex-wrap">
          <li v-for="(menuItem, index) in menuItems" :key="index" class="py-4 hover:bg-teal-500 px-2"
          :class="{
            'hover:bg-teal-500': menuItem.name !== 'Sales & Offers' && menuItem.name !== 'Outdoors' && menuItem.name !== 'New',
            'bg-red-500': menuItem.name === 'Sales & Offers',
            'bg-pink-600': menuItem.name === 'Outdoors',
            'bg-blue-500': menuItem.name === 'New'
          }"
          >
            <a :href="menuItem.link" class="menu-item text-white text-center leading-4 capitalize font-bold z-50 text-base">{{ menuItem.name }}</a>
          </li>
        </ul>
      </nav>
    </div>
  </div>
</template>

<script setup>
const menuItems = [
  { name: "All Tiles", link: "#" },
  { name: "Bathroom", link: "#" },
  { name: "Kitchen", link: "#" },
  { name: "Floor", link: "#" },
  { name: "Wall", link: "#" },
  { name: "Outdoors", link: "#" },
  { name: "Luxury Vinyl", link: "#" },
  { name: "Laminate", link: "#" },
  { name: "Real Wood", link: "#" },
  { name: "New", link: "#" },
  { name: "Adhesive", link: "#" },
  { name: "Accessories", link: "#" },
  { name: "Sales & Offers", link: "#" },
  { name: "Style & Advice", link: "#" },
  { name: "Offers", link: "#" },
  { name: "Accessories", link: "#" },
];
</script>

<style scoped>

</style>
