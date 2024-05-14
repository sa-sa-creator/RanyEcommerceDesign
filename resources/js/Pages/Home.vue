<script setup>
import { onMounted } from "vue";
import { initFlowbite } from "flowbite";
import Footer from "@/Pages/Footer.vue";
import Header from "@/Pages/Header.vue";
import FilterCategory from "./FilterCategory.vue";
// initialize components based on data attribute selectors
onMounted(() => {
    initFlowbite();
});
</script>

<template>
    <div>
        <!-- hero - start -->
        <div class="bg-white">
            <Header></Header>
            <!-- filter categories -->
            <FilterCategory></FilterCategory>
        </div>
        <!-- hero - end -->

        <!-- product-grid - start -->
        <div class="py-6 bg-white sm:py-8 lg:pb-12">
            <div class="px-4 mx-auto max-w-screen-2xl md:px-8">
                <h6 class="pb-10 text-2xl font-bold">All Products</h6>
                <div
                    class="grid gap-x-4 gap-y-8 sm:grid-cols-2 md:gap-x-6 lg:grid-cols-3 xl:grid-cols-4"
                >
                    <!-- product - start -->
                    <div>
                        <a
                            href="#"
                            class="relative block h-64 mb-2 overflow-hidden bg-gray-100 rounded-lg shadow-lg group lg:mb-3"
                        >
                            <img
                                src="https://images.unsplash.com/photo-1552374196-1ab2a1c593e8?auto=format&q=75&fit=crop&crop=top&w=600&h=700"
                                loading="lazy"
                                alt="Photo by Austin Wade"
                                class="object-cover object-center w-full h-full transition duration-200 group-hover:scale-110"
                            />

                            <div class="absolute left-0 flex gap-2 bottom-2">
                                <span
                                    class="rounded-r-lg bg-red-500 px-3 py-1.5 text-sm font-semibold uppercase tracking-wider text-white"
                                    >-50%</span
                                >
                                <span
                                    class="rounded-lg bg-white px-3 py-1.5 text-sm font-bold uppercase tracking-wider text-gray-800"
                                    >New</span
                                >
                            </div>
                        </a>

                        <div
                            class="flex items-start justify-between gap-2 px-2"
                        >
                            <div class="flex flex-col">
                                <a
                                    href="#"
                                    class="text-lg font-bold text-gray-800 transition duration-100 hover:text-gray-500 lg:text-xl"
                                    >Fancy Outfit</a
                                >
                                <span class="text-gray-500"
                                    >by Fancy Brand</span
                                >
                            </div>

                            <div class="flex flex-col items-end">
                                <span class="font-bold text-gray-600 lg:text-lg"
                                    >$19.99</span
                                >
                                <span class="text-sm text-red-500 line-through"
                                    >$39.99</span
                                >
                            </div>
                        </div>
                    </div>
                    <!-- product - end -->

                    <!-- product - start -->
                    <div>
                        <a
                            href="#"
                            class="relative block h-64 mb-2 overflow-hidden bg-gray-100 rounded-lg shadow-lg group lg:mb-3"
                        >
                            <img
                                src="https://images.unsplash.com/photo-1523359346063-d879354c0ea5?auto=format&q=75&fit=crop&crop=top&w=600&h=700"
                                loading="lazy"
                                alt="Photo by Nick Karvounis"
                                class="object-cover object-center w-full h-full transition duration-200 group-hover:scale-110"
                            />
                        </a>

                        <div
                            class="flex items-start justify-between gap-2 px-2"
                        >
                            <div class="flex flex-col">
                                <a
                                    href="#"
                                    class="text-lg font-bold text-gray-800 transition duration-100 hover:text-gray-500 lg:text-xl"
                                    >Cool Outfit</a
                                >
                                <span class="text-gray-500">by Cool Brand</span>
                            </div>

                            <div class="flex flex-col items-end">
                                <span class="font-bold text-gray-600 lg:text-lg"
                                    >$29.99</span
                                >
                            </div>
                        </div>
                    </div>
                    <!-- product - end -->

                    <!-- product - start -->
                    <div>
                        <a
                            href="#"
                            class="relative block h-64 mb-2 overflow-hidden bg-gray-100 rounded-lg shadow-lg group lg:mb-3"
                        >
                            <img
                                src="https://images.unsplash.com/photo-1548286978-f218023f8d18?auto=format&q=75&fit=crop&crop=top&w=600&h=700"
                                loading="lazy"
                                alt="Photo by Austin Wade"
                                class="object-cover object-center w-full h-full transition duration-200 group-hover:scale-110"
                            />
                        </a>

                        <div
                            class="flex items-start justify-between gap-2 px-2"
                        >
                            <div class="flex flex-col">
                                <a
                                    href="#"
                                    class="text-lg font-bold text-gray-800 transition duration-100 hover:text-gray-500 lg:text-xl"
                                    >Nice Outfit</a
                                >
                                <span class="text-gray-500">by Nice Brand</span>
                            </div>

                            <div class="flex flex-col items-end">
                                <span class="font-bold text-gray-600 lg:text-lg"
                                    >$35.00</span
                                >
                            </div>
                        </div>
                    </div>
                    <!-- product - end -->

                    <!-- product - start -->
                    <div>
                        <a
                            href="#"
                            class="relative block h-64 mb-2 overflow-hidden bg-gray-100 rounded-lg shadow-lg group lg:mb-3"
                        >
                            <img
                                src="https://images.unsplash.com/photo-1566207274740-0f8cf6b7d5a5?auto=format&q=75&fit=crop&crop=top&w=600&h=700"
                                loading="lazy"
                                alt="Photo by Vladimir Fedotov"
                                class="object-cover object-center w-full h-full transition duration-200 group-hover:scale-110"
                            />
                        </a>

                        <div
                            class="flex items-start justify-between gap-2 px-2"
                        >
                            <div class="flex flex-col">
                                <a
                                    href="#"
                                    class="text-lg font-bold text-gray-800 transition duration-100 hover:text-gray-500 lg:text-xl"
                                    >Lavish Outfit</a
                                >
                                <span class="text-gray-500"
                                    >by Lavish Brand</span
                                >
                            </div>

                            <div class="flex flex-col items-end">
                                <span class="font-bold text-gray-600 lg:text-lg"
                                    >$49.99</span
                                >
                            </div>
                        </div>
                    </div>
                    <!-- product - end -->
                </div>
            </div>
        </div>
        <!-- product-grid - end -->
        <Footer></Footer>
    </div>
</template>
