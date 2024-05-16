<template>
<div>
    <!-- First footer -->
    <footer class="bg-[#606060] px-4">
        <div class="container mx-auto">
            <div class="grid grid-cols-12 py-5">
                <!-- Loop through footerData to generate columns -->
                <div v-for="(column, index) in footerData" :key="index" :class="column.class">
                    <h2 class="text-white text-xl font-bold pb-4 pt-6">{{ column.title }}</h2>
                    <ul>
                        <!-- Loop through column items -->
                        <li v-for="(item, idx) in column.items" :key="idx" class="pb-2 my-2">
                            <a :href="item.link" class="text-base text-white">{{ item.text }}</a>
                        </li>
                    </ul>
                </div>
                <div class="col-span-12 lg:col-span-2 md:col-span-6">
                    <h2 class="text-white text-xl font-bold pb-4 pt-6">Follow Us</h2>
                    <div class="flex gap-3 flex-wrap">
                        <!-- Loop through social media icons -->
                        <div v-for="(socialMedia, index) in socialMediaIcons" :key="index" :class="socialMedia.containerClass">
                            <a :href="socialMedia.link" target="_blank" rel="noopener noreferrer">
                                <div :class="socialMedia.iconContainerClass">
                                    <i :class="socialMedia.iconClass"></i>
                                </div>
                            </a>
                        </div>
                    </div>
                    <div class="group flex mt-8 justify-center items-center gap-4 bg-[#9D9D9D] hover:bg-[#434243] rounded-lg p-3 max-w-[360px]">
                        <i class="fa-solid fa-location-dot text-gray-700 text-xl group-hover:text-white"></i>
                        <p class="text-gray-700 text-xl font-bold group-hover:text-white">Find your local store</p>
                    </div>
                    <h2 class="text-white text-xl font-bold pb-4 pt-6">Accepted Cards</h2>
                    <img :src="paymentImage" alt="">
                </div>
            </div>
        </div>
    </footer>

    <!-- Second footer -->
    <footer class="bg-[#444444]">
        <p class="text-center text-base text-white py-5">{{ copyright }}</p>
    </footer>
</div>
</template>

<script>
import payment from "@/assets/payments.svg"
export default {
    data() {
        return {
            footerData: [{
                    title: 'Customer Info',
                    class: 'col-span-12 lg:col-span-3 md:col-span-6',
                    items: [{
                            text: 'Clearance & Offers',
                            link: '#'
                        },
                        {
                            text: 'Contact Us',
                            link: '#'
                        },
                        {
                            text: 'Delivery',
                            link: '#'
                        },
                        {
                            text: 'FAQ',
                            link: '#'
                        },
                        {
                            text: 'Discount & Vouchers',
                            link: '#'
                        },
                        {
                            text: 'Returns & Exchange Policy',
                            link: '#'
                        },
                        {
                            text: 'Tile Terms Glossary',
                            link: '#'
                        },
                        {
                            text: 'Samples',
                            link: '#'
                        }
                    ]
                },
                {
                    title: 'Popular Tiles',
                    class: 'col-span-12 lg:col-span-3 md:col-span-6',
                    items: [{
                            text: 'Bathroom Tiles',
                            link: '#'
                        },
                        {
                            text: 'Kitchen Tiles',
                            link: '#'
                        },
                        {
                            text: 'Floor Tiles',
                            link: '#'
                        },
                        {
                            text: 'Wall Tiles',
                            link: '#'
                        },
                        {
                            text: 'Mosaic Tiles',
                            link: '#'
                        },
                        {
                            text: 'Metro Subway Tiles',
                            link: '#'
                        },
                        {
                            text: 'Porcelain Tiles',
                            link: '#'
                        },
                        {
                            text: 'Quartz Tiles',
                            link: '#'
                        }
                    ]
                },
                {
                    title: 'Company',
                    class: 'col-span-12 lg:col-span-2 md:col-span-6',
                    items: [{
                            text: 'About Us',
                            link: '#'
                        },
                        {
                            text: 'Careers',
                            link: '#'
                        },
                        {
                            text: 'Press',
                            link: '#'
                        },
                        {
                            text: 'Terms Of Use',
                            link: '#'
                        },
                        {
                            text: 'Terms & Conditions',
                            link: '#'
                        },
                        {
                            text: 'Privacy Policy',
                            link: '#'
                        },
                        {
                            text: 'Sitemap',
                            link: '#'
                        },
                        {
                            text: 'Our Flagship Showrooms',
                            link: '#'
                        },
                        {
                            text: 'Bathroom Mountain',
                            link: '#'
                        }
                    ]
                }
            ],
            copyright: '© 2024 Tile Mountain Ltd TMBM1',
            paymentImage: payment,
            socialMediaIcons: [{
                    link: "https://www.facebook.com",
                    iconClass: "fa-brands fa-facebook-f text-4xl group-hover:text-white",
                    containerClass: "group h-14 w-14 bg-[#9D9D9D] hover:bg-[#1877F2] flex justify-center items-center rounded-full",
                    iconContainerClass: ""
                },
                {
                    link: "https://twitter.com",
                    iconClass: "fa-brands fa-twitter text-4xl group-hover:text-white",
                    containerClass: "group h-14 w-14 bg-[#9D9D9D] hover:bg-[#1DA1F2] flex justify-center items-center rounded-full",
                    iconContainerClass: ""
                },
                {
                    link: "https://www.pinterest.com",
                    iconClass: "fa-brands fa-pinterest text-4xl group-hover:text-white",
                    containerClass: "group h-14 w-14 bg-[#9D9D9D] hover:bg-[#E60023] flex justify-center items-center rounded-full",
                    iconContainerClass: ""
                },
                {
                    link: "https://www.youtube.com",
                    iconClass: "fa-brands fa-youtube text-4xl group-hover:text-white",
                    containerClass: "group h-14 w-14 bg-[#9D9D9D] hover:bg-[#FF0000] flex justify-center items-center rounded-full",
                    iconContainerClass: ""
                },
                {
                    link: "https://www.linkedin.com",
                    iconClass: "fa-brands fa-linkedin text-4xl group-hover:text-white",
                    containerClass: "group h-14 w-14 bg-[#9D9D9D] hover:bg-[#0077B5] flex justify-center items-center rounded-full",
                    iconContainerClass: ""
                },
                {
                    link: "https://www.instagram.com",
                    iconClass: "fa-brands fa-instagram text-4xl group-hover:text-white",
                    containerClass: "group h-14 w-14 bg-[#9D9D9D] hover:bg-[#e1306c] flex justify-center items-center rounded-full",
                    iconContainerClass: ""
                }
            ],
        };
    }
};
</script>
