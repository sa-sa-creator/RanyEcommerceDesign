<script setup>
import { onMounted } from "vue";
import { initFlowbite } from "flowbite";

// initialize components based on data attribute selectors
onMounted(() => {
    initFlowbite();
});
</script>

<template>
    <div>
        <header class="antialiased">
            <nav
                class="bg-slate-100 border-gray-200 px-4 lg:px-20 py-2.5 dark:bg-gray-800"
            >
                <div class="flex flex-wrap items-center justify-between">
                    <div class="flex items-center justify-start">
                        <a href="https://flowbite.com" class="flex mr-4">
                            <img
                                src="https://flowbite.s3.amazonaws.com/logo.svg"
                                class="h-8 mr-3"
                                alt="FlowBite Logo"
                            />
                            <span
                                class="self-center text-2xl font-semibold whitespace-nowrap dark:text-white"
                                >Flowbite</span
                            >
                        </a>
                    </div>

                    <div class="flex items-center lg:order-2">
                        <button
                            id="toggleSidebarMobileSearch"
                            type="button"
                            class="p-2 text-gray-500 rounded-lg lg:hidden hover:text-gray-900 hover:bg-gray-100 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-white"
                        >
                            <span class="sr-only">Search</span>
                            <!-- Search icon -->
                            <svg
                                class="w-4 h-4"
                                aria-hidden="true"
                                xmlns="http://www.w3.org/2000/svg"
                                fill="none"
                                viewBox="0 0 20 20"
                            >
                                <path
                                    stroke="currentColor"
                                    stroke-linecap="round"
                                    stroke-linejoin="round"
                                    stroke-width="2"
                                    d="m19 19-4-4m0-7A7 7 0 1 1 1 8a7 7 0 0 1 14 0Z"
                                />
                            </svg>
                        </button>
                        <!-- Notifications -->
                        <button
                            type="button"
                            data-dropdown-toggle="notification-dropdown"
                            class="relative inline-flex items-center mr-1 text-sm font-medium text-center rounded-lg hover:text-gray-900 hover:bg-gray-100 dark:text-gray-400 dark:hover:text-white dark:hover:bg-gray-700 focus:ring-4 focus:ring-gray-300 dark:focus:ring-gray-600 focus:outline-none"
                        >
                            <span class="sr-only">View notifications</span>
                            <!-- Bell icon -->

                            <svg
                                class="w-8"
                                fill="#000000"
                                version="1.1"
                                viewBox="144 144 512 512"
                                xmlns="http://www.w3.org/2000/svg"
                            >
                                <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
                                <g
                                    id="SVGRepo_tracerCarrier"
                                    stroke-linecap="round"
                                    stroke-linejoin="round"
                                ></g>
                                <g id="SVGRepo_iconCarrier">
                                    <path
                                        d="m376.91 382.09c-2.2227 2.2109-3.4727 5.2109-3.4766 8.3438-0.007813 3.1328 1.2305 6.1406 3.4414 8.3594l59.953 60.199 0.011719 0.007812c0.54688 0.54297 1.1406 1.0312 1.7812 1.4609 0.14844 0.097656 0.31641 0.15625 0.46875 0.25391h-0.003906c0.5 0.31641 1.0234 0.59766 1.5625 0.83594 0.23437 0.097657 0.48437 0.14453 0.72656 0.22656 0.48438 0.18359 0.98047 0.33203 1.4844 0.44922 1.543 0.31641 3.1328 0.31641 4.6758 0 0.57031-0.125 1.1328-0.29687 1.6797-0.51172 0.17188-0.0625 0.35547-0.09375 0.52344-0.16406h0.003907c0.65625-0.27734 1.2852-0.61328 1.8828-1.0078l0.14453-0.078125c0.64453-0.43359 1.2461-0.92578 1.793-1.4766l59.934-60.199c4.4883-4.6367 4.418-12.023-0.15625-16.578-4.5742-4.5547-11.957-4.5898-16.578-0.082032l-39.754 39.93v-176.85c0-6.5234-5.2852-11.809-11.809-11.809-6.5195 0-11.809 5.2852-11.809 11.809v176.86l-39.781-39.934c-2.207-2.2188-5.2109-3.4727-8.3398-3.4805-3.1328-0.003907-6.1406 1.2305-8.3594 3.4414zm243.26-53.965c-5.2188-6.4648-13.09-10.215-21.402-10.199h-82.09c-6.5195 0-11.809 5.2891-11.809 11.809s5.2891 11.809 11.809 11.809h82.09c1.1875 0 2.3125 0.53516 3.0586 1.457 0.74609 0.91797 1.0391 2.1289 0.79297 3.2891l-27.727 131.23c-1.1367 5.2891-4.0508 10.031-8.2539 13.438s-9.4414 5.2734-14.852 5.293h-219.7c-5.25 0.003906-10.355-1.7461-14.5-4.9727-4.1445-3.2227-7.0977-7.7383-8.3906-12.828l-34.773-136.91h100.55c6.5195 0 11.809-5.2891 11.809-11.809s-5.2891-11.809-11.809-11.809h-106.55l-24.809-97.668c-1.5078-5.9414-4.9492-11.211-9.7891-14.973-4.8359-3.7617-10.789-5.8047-16.918-5.8008h-31.438c-6.5195 0-11.805 5.2852-11.805 11.809 0 6.5195 5.2852 11.809 11.805 11.809h31.438c1.8008 0 3.3711 1.2188 3.8164 2.9688l65.586 258.19c2.5781 10.184 8.4805 19.215 16.773 25.664 8.2891 6.4492 18.496 9.9453 29 9.9414h219.7c10.82-0.039063 21.301-3.7773 29.707-10.59 8.4062-6.8164 14.23-16.297 16.504-26.875l27.73-131.23c1.7344-8.1289-0.30859-16.605-5.5586-23.051zm-95.359 209.41c-8.3516 0-16.359 3.3203-22.266 9.2227-5.9023 5.9062-9.2227 13.914-9.2227 22.266 0 8.3516 3.3203 16.359 9.2227 22.266 5.9062 5.9062 13.914 9.2227 22.266 9.2227 8.3516 0 16.359-3.3164 22.266-9.2227s9.2227-13.914 9.2227-22.266c-0.007813-8.3477-3.3281-16.352-9.2305-22.254-5.9062-5.9023-13.91-9.2227-22.258-9.2344zm0 39.359c-3.1836 0-6.0547-1.918-7.2734-4.8594s-0.54297-6.3242 1.707-8.5781c2.2539-2.25 5.6367-2.9258 8.5781-1.707 2.9414 1.2188 4.8594 4.0898 4.8594 7.2734-0.003907 4.3477-3.5234 7.8672-7.8711 7.8711zm-174.97-39.359c-8.3516 0-16.359 3.3203-22.266 9.2227-5.9023 5.9062-9.2227 13.914-9.2227 22.266 0 8.3516 3.3203 16.359 9.2227 22.266 5.9062 5.9062 13.914 9.2227 22.266 9.2227 8.3516 0 16.363-3.3164 22.266-9.2227 5.9062-5.9062 9.2227-13.914 9.2227-22.266-0.007813-8.3477-3.3281-16.352-9.2305-22.254-5.9062-5.9023-13.91-9.2227-22.258-9.2344zm0 39.359c-3.1836 0-6.0547-1.918-7.2734-4.8594-1.2148-2.9414-0.54297-6.3242 1.707-8.5781 2.2539-2.25 5.6367-2.9258 8.582-1.707 2.9414 1.2188 4.8594 4.0898 4.8594 7.2734-0.007813 4.3477-3.5273 7.8672-7.875 7.8711z"
                                    ></path>
                                </g>
                            </svg>
                            <div
                                class="absolute inline-flex items-center justify-center w-auto text-xs font-bold text-white bg-red-500 border-2 border-red-500 rounded-full -top-2 -end-2 dark:border-gray-900"
                            >
                                100
                            </div>
                        </button>
                        <!-- Dropdown menu -->
                        <div
                            class="z-50 hidden max-w-sm my-4 overflow-hidden text-base list-none bg-white divide-y divide-gray-100 rounded shadow-lg dark:divide-gray-600 dark:bg-gray-700"
                            id="notification-dropdown"
                        >
                            <div
                                class="block px-4 py-2 text-base font-medium text-center text-gray-700 bg-gray-50 dark:bg-gray-700 dark:text-gray-400"
                            >
                                Notifications
                            </div>
                            <div>
                                <a
                                    href="#"
                                    class="flex px-4 py-3 border-b hover:bg-gray-100 dark:hover:bg-gray-600 dark:border-gray-600"
                                >
                                    <div class="flex-shrink-0">
                                        <img
                                            class="rounded-full w-11 h-11"
                                            src="https://flowbite.s3.amazonaws.com/blocks/marketing-ui/avatars/bonnie-green.png"
                                            alt="Bonnie Green avatar"
                                        />
                                        <div
                                            class="absolute flex items-center justify-center w-5 h-5 ml-6 -mt-5 border border-white rounded-full bg-primary-700 dark:border-gray-700"
                                        >
                                            <svg
                                                class="w-2 h-2 text-white"
                                                aria-hidden="true"
                                                xmlns="http://www.w3.org/2000/svg"
                                                fill="currentColor"
                                                viewBox="0 0 18 18"
                                            >
                                                <path
                                                    d="M15.977.783A1 1 0 0 0 15 0H3a1 1 0 0 0-.977.783L.2 9h4.239a2.99 2.99 0 0 1 2.742 1.8 1.977 1.977 0 0 0 3.638 0A2.99 2.99 0 0 1 13.561 9H17.8L15.977.783ZM6 2h6a1 1 0 1 1 0 2H6a1 1 0 0 1 0-2Zm7 5H5a1 1 0 0 1 0-2h8a1 1 0 1 1 0 2Z"
                                                />
                                                <path
                                                    d="M1 18h16a1 1 0 0 0 1-1v-6h-4.439a.99.99 0 0 0-.908.6 3.978 3.978 0 0 1-7.306 0 .99.99 0 0 0-.908-.6H0v6a1 1 0 0 0 1 1Z"
                                                />
                                            </svg>
                                        </div>
                                    </div>
                                    <div class="w-full pl-3">
                                        <div
                                            class="text-gray-500 font-normal text-sm mb-1.5 dark:text-gray-400"
                                        >
                                            New message from
                                            <span
                                                class="font-semibold text-gray-900 dark:text-white"
                                                >Bonnie Green</span
                                            >: "Hey, what's up? All set for the
                                            presentation?"
                                        </div>
                                        <div
                                            class="text-xs font-medium text-primary-700 dark:text-primary-400"
                                        >
                                            a few moments ago
                                        </div>
                                    </div>
                                </a>
                                <a
                                    href="#"
                                    class="flex px-4 py-3 border-b hover:bg-gray-100 dark:hover:bg-gray-600 dark:border-gray-600"
                                >
                                    <div class="flex-shrink-0">
                                        <img
                                            class="rounded-full w-11 h-11"
                                            src="https://flowbite.s3.amazonaws.com/blocks/marketing-ui/avatars/jese-leos.png"
                                            alt="Jese Leos avatar"
                                        />
                                        <div
                                            class="absolute flex items-center justify-center w-5 h-5 ml-6 -mt-5 bg-gray-900 border border-white rounded-full dark:border-gray-700"
                                        >
                                            <svg
                                                class="w-2 h-2 text-white"
                                                aria-hidden="true"
                                                xmlns="http://www.w3.org/2000/svg"
                                                fill="currentColor"
                                                viewBox="0 0 20 18"
                                            >
                                                <path
                                                    d="M6.5 9a4.5 4.5 0 1 0 0-9 4.5 4.5 0 0 0 0 9ZM8 10H5a5.006 5.006 0 0 0-5 5v2a1 1 0 0 0 1 1h11a1 1 0 0 0 1-1v-2a5.006 5.006 0 0 0-5-5Zm11-3h-2V5a1 1 0 0 0-2 0v2h-2a1 1 0 1 0 0 2h2v2a1 1 0 0 0 2 0V9h2a1 1 0 1 0 0-2Z"
                                                />
                                            </svg>
                                        </div>
                                    </div>
                                    <div class="w-full pl-3">
                                        <div
                                            class="text-gray-500 font-normal text-sm mb-1.5 dark:text-gray-400"
                                        >
                                            <span
                                                class="font-semibold text-gray-900 dark:text-white"
                                                >Jese leos</span
                                            >
                                            and
                                            <span
                                                class="font-medium text-gray-900 dark:text-white"
                                                >5 others</span
                                            >
                                            started following you.
                                        </div>
                                        <div
                                            class="text-xs font-medium text-primary-700 dark:text-primary-400"
                                        >
                                            10 minutes ago
                                        </div>
                                    </div>
                                </a>
                                <a
                                    href="#"
                                    class="flex px-4 py-3 border-b hover:bg-gray-100 dark:hover:bg-gray-600 dark:border-gray-600"
                                >
                                    <div class="flex-shrink-0">
                                        <img
                                            class="rounded-full w-11 h-11"
                                            src="https://flowbite.s3.amazonaws.com/blocks/marketing-ui/avatars/joseph-mcfall.png"
                                            alt="Joseph McFall avatar"
                                        />
                                        <div
                                            class="absolute flex items-center justify-center w-5 h-5 ml-6 -mt-5 bg-red-600 border border-white rounded-full dark:border-gray-700"
                                        >
                                            <svg
                                                class="w-2 h-2 text-white"
                                                aria-hidden="true"
                                                xmlns="http://www.w3.org/2000/svg"
                                                fill="currentColor"
                                                viewBox="0 0 20 18"
                                            >
                                                <path
                                                    d="M17.947 2.053a5.209 5.209 0 0 0-3.793-1.53A6.414 6.414 0 0 0 10 2.311 6.482 6.482 0 0 0 5.824.5a5.2 5.2 0 0 0-3.8 1.521c-1.915 1.916-2.315 5.392.625 8.333l7 7a.5.5 0 0 0 .708 0l7-7a6.6 6.6 0 0 0 2.123-4.508 5.179 5.179 0 0 0-1.533-3.793Z"
                                                />
                                            </svg>
                                        </div>
                                    </div>
                                    <div class="w-full pl-3">
                                        <div
                                            class="text-gray-500 font-normal text-sm mb-1.5 dark:text-gray-400"
                                        >
                                            <span
                                                class="font-semibold text-gray-900 dark:text-white"
                                                >Joseph Mcfall</span
                                            >
                                            and
                                            <span
                                                class="font-medium text-gray-900 dark:text-white"
                                                >141 others</span
                                            >
                                            love your story. See it and view
                                            more stories.
                                        </div>
                                        <div
                                            class="text-xs font-medium text-primary-700 dark:text-primary-400"
                                        >
                                            44 minutes ago
                                        </div>
                                    </div>
                                </a>
                                <a
                                    href="#"
                                    class="flex px-4 py-3 border-b hover:bg-gray-100 dark:hover:bg-gray-600 dark:border-gray-600"
                                >
                                    <div class="flex-shrink-0">
                                        <img
                                            class="rounded-full w-11 h-11"
                                            src="https://flowbite.s3.amazonaws.com/blocks/marketing-ui/avatars/roberta-casas.png"
                                            alt="Roberta Casas image"
                                        />
                                        <div
                                            class="absolute flex items-center justify-center w-5 h-5 ml-6 -mt-5 bg-green-400 border border-white rounded-full dark:border-gray-700"
                                        >
                                            <svg
                                                class="w-2 h-2 text-white"
                                                aria-hidden="true"
                                                xmlns="http://www.w3.org/2000/svg"
                                                fill="currentColor"
                                                viewBox="0 0 20 18"
                                            >
                                                <path
                                                    d="M18 0H2a2 2 0 0 0-2 2v9a2 2 0 0 0 2 2h2v4a1 1 0 0 0 1.707.707L10.414 13H18a2 2 0 0 0 2-2V2a2 2 0 0 0-2-2Zm-5 4h2a1 1 0 1 1 0 2h-2a1 1 0 1 1 0-2ZM5 4h5a1 1 0 1 1 0 2H5a1 1 0 0 1 0-2Zm2 5H5a1 1 0 0 1 0-2h2a1 1 0 0 1 0 2Zm9 0h-6a1 1 0 0 1 0-2h6a1 1 0 1 1 0 2Z"
                                                />
                                            </svg>
                                        </div>
                                    </div>
                                    <div class="w-full pl-3">
                                        <div
                                            class="text-gray-500 font-normal text-sm mb-1.5 dark:text-gray-400"
                                        >
                                            <span
                                                class="font-semibold text-gray-900 dark:text-white"
                                                >Leslie Livingston</span
                                            >
                                            mentioned you in a comment:
                                            <span
                                                class="font-medium text-primary-700 dark:text-primary-500"
                                                >@bonnie.green</span
                                            >
                                            what do you say?
                                        </div>
                                        <div
                                            class="text-xs font-medium text-primary-700 dark:text-primary-400"
                                        >
                                            1 hour ago
                                        </div>
                                    </div>
                                </a>
                                <a
                                    href="#"
                                    class="flex px-4 py-3 hover:bg-gray-100 dark:hover:bg-gray-600"
                                >
                                    <div class="flex-shrink-0">
                                        <img
                                            class="rounded-full w-11 h-11"
                                            src="https://flowbite.s3.amazonaws.com/blocks/marketing-ui/avatars/robert-brown.png"
                                            alt="Robert image"
                                        />
                                        <div
                                            class="absolute flex items-center justify-center w-5 h-5 ml-6 -mt-5 bg-purple-500 border border-white rounded-full dark:border-gray-700"
                                        >
                                            <svg
                                                class="w-2 h-2 text-white"
                                                aria-hidden="true"
                                                xmlns="http://www.w3.org/2000/svg"
                                                fill="currentColor"
                                                viewBox="0 0 20 14"
                                            >
                                                <path
                                                    d="M11 0H2a2 2 0 0 0-2 2v10a2 2 0 0 0 2 2h9a2 2 0 0 0 2-2V2a2 2 0 0 0-2-2Zm8.585 1.189a.994.994 0 0 0-.9-.138l-2.965.983a1 1 0 0 0-.685.949v8a1 1 0 0 0 .675.946l2.965 1.02a1.013 1.013 0 0 0 1.032-.242A1 1 0 0 0 20 12V2a1 1 0 0 0-.415-.811Z"
                                                />
                                            </svg>
                                        </div>
                                    </div>
                                    <div class="w-full pl-3">
                                        <div
                                            class="text-gray-500 font-normal text-sm mb-1.5 dark:text-gray-400"
                                        >
                                            <span
                                                class="font-semibold text-gray-900 dark:text-white"
                                                >Robert Brown</span
                                            >
                                            posted a new video: Glassmorphism -
                                            learn how to implement the new
                                            design trend.
                                        </div>
                                        <div
                                            class="text-xs font-medium text-primary-700 dark:text-primary-400"
                                        >
                                            3 hours ago
                                        </div>
                                    </div>
                                </a>
                            </div>
                            <a
                                href="#"
                                class="block py-2 text-base font-medium text-center text-gray-900 bg-gray-50 hover:bg-gray-100 dark:bg-gray-700 dark:text-white dark:hover:underline"
                            >
                                <div class="inline-flex items-center">
                                    <svg
                                        aria-hidden="true"
                                        class="w-5 h-5 mr-2"
                                        fill="currentColor"
                                        viewBox="0 0 20 20"
                                        xmlns="http://www.w3.org/2000/svg"
                                    >
                                        <path
                                            d="M10 12a2 2 0 100-4 2 2 0 000 4z"
                                        ></path>
                                        <path
                                            fill-rule="evenodd"
                                            d="M.458 10C1.732 5.943 5.522 3 10 3s8.268 2.943 9.542 7c-1.274 4.057-5.064 7-9.542 7S1.732 14.057.458 10zM14 10a4 4 0 11-8 0 4 4 0 018 0z"
                                            clip-rule="evenodd"
                                        ></path>
                                    </svg>
                                    View all
                                </div>
                            </a>
                        </div>
                        <!-- Apps -->

                        <button
                            type="button"
                            class="flex mx-3 text-sm rounded-full md:mr-0 focus:ring-4 focus:ring-gray-300 dark:focus:ring-gray-600"
                            id="user-menu-button"
                            aria-expanded="false"
                            data-dropdown-toggle="dropdown"
                        >
                            <span class="sr-only">Open user menu</span>
                            <svg
                                class="w-8"
                                fill="#000000"
                                version="1.1"
                                viewBox="144 144 512 512"
                                xmlns="http://www.w3.org/2000/svg"
                            >
                                <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
                                <g
                                    id="SVGRepo_tracerCarrier"
                                    stroke-linecap="round"
                                    stroke-linejoin="round"
                                ></g>
                                <g id="SVGRepo_iconCarrier">
                                    <path
                                        d="m400 160.69c66.082 0 125.92 26.797 169.21 70.09 43.297 43.297 70.09 103.14 70.09 169.21 0 66.082-26.797 125.92-70.09 169.21-43.297 43.297-103.14 70.09-169.21 70.09-66.082 0-125.92-26.797-169.21-70.09-43.297-43.297-70.09-103.14-70.09-169.21 0-66.082 26.797-125.92 70.09-169.21 43.297-43.297 103.14-70.09 169.21-70.09zm-140.4 407.13c35.949 33.238 91.941 51.336 140.4 51.336 48.98 0 103.98-18.066 140.47-51.379 5.0742-4.6602 8.0039-9.668 8.6953-14.816 0.67969-5.1641-0.76953-10.938-4.4141-17.137-17.715-25.742-33.836-43.945-48.98-55.477-13.828-10.543-26.684-15.352-39.145-15.227-18.465 0.92969-98.059 2.5234-112.41 0.011719-12.723-0.34375-25.844 4.4375-39.977 15.215-15.18 11.566-31.348 29.832-49.117 55.684-3.5781 6.125-4.9805 11.816-4.2852 16.93 0.69531 5.1523 3.6523 10.168 8.7539 14.859zm-27.82-27.348c1.2031-4.9805 3.3086-10.039 6.3359-15.121l0.32031-0.50391c19.055-27.758 36.695-47.586 53.609-60.469 17.895-13.645 35.133-19.719 52.414-19.316l111.78-0.011718c17.047-0.23047 34.066 5.8594 51.727 19.328 16.91 12.883 34.562 32.715 53.621 60.465l0.35156 0.55469c3.0039 5.0508 5.1016 10.086 6.2969 15.066 31.789-38.035 50.926-87.016 50.926-140.46 0-60.516-24.535-115.32-64.188-154.97-39.656-39.656-94.453-64.188-154.97-64.188s-115.32 24.535-154.97 64.188c-39.656 39.656-64.188 94.453-64.188 154.97 0 53.449 19.145 102.44 50.938 140.48zm168.23-127.15c16.477 0 31.402-6.6836 42.203-17.484 10.793-10.793 17.477-25.723 17.477-42.207 0-16.5-6.6719-31.43-17.441-42.195-10.805-10.812-25.734-17.484-42.238-17.484-16.484 0-31.414 6.6836-42.207 17.477l-0.52344 0.48828c-10.496 10.734-16.965 25.461-16.965 41.715 0 16.512 6.6719 31.441 17.441 42.207 10.844 10.801 25.773 17.484 42.254 17.484zm56.445-3.2383c-14.449 14.449-34.406 23.387-56.445 23.387-22.047 0-42.012-8.9375-56.457-23.387-14.438-14.484-23.387-34.449-23.387-56.453 0-21.695 8.707-41.414 22.828-55.836l0.56641-0.61328c14.438-14.438 34.406-23.379 56.453-23.379 21.969 0 41.914 8.9336 56.375 23.363l0.042969 0.046875c14.473 14.477 23.41 34.438 23.41 56.418 0 22.047-8.9453 42.016-23.379 56.453z"
                                    ></path>
                                </g>
                            </svg>
                        </button>
                        <!-- Dropdown menu -->
                        <div
                            class="z-50 hidden w-56 my-4 text-base list-none bg-white divide-y divide-gray-100 rounded shadow dark:bg-gray-700 dark:divide-gray-600"
                            id="dropdown"
                        >
                            <div class="px-4 py-3">
                                <span
                                    class="block text-sm font-semibold text-gray-900 dark:text-white"
                                    >Neil sims</span
                                >
                                <span
                                    class="block text-sm text-gray-500 truncate dark:text-gray-400"
                                    >name@flowbite.com</span
                                >
                            </div>
                            <ul
                                class="py-1 text-gray-500 dark:text-gray-400"
                                aria-labelledby="dropdown"
                            >
                                <li>
                                    <a
                                        href="#"
                                        class="block px-4 py-2 text-sm hover:bg-gray-100 dark:hover:bg-gray-600 dark:text-gray-400 dark:hover:text-white"
                                        >My profile</a
                                    >
                                </li>
                                <li>
                                    <a
                                        href="#"
                                        class="block px-4 py-2 text-sm hover:bg-gray-100 dark:hover:bg-gray-600 dark:text-gray-400 dark:hover:text-white"
                                        >Account settings</a
                                    >
                                </li>
                            </ul>
                            <ul
                                class="py-1 text-gray-500 dark:text-gray-400"
                                aria-labelledby="dropdown"
                            >
                                <li>
                                    <a
                                        href="#"
                                        class="flex items-center px-4 py-2 text-sm hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white"
                                    >
                                        <svg
                                            class="w-4 h-4 mr-2 text-gray-400"
                                            aria-hidden="true"
                                            xmlns="http://www.w3.org/2000/svg"
                                            fill="currentColor"
                                            viewBox="0 0 20 18"
                                        >
                                            <path
                                                d="M17.947 2.053a5.209 5.209 0 0 0-3.793-1.53A6.414 6.414 0 0 0 10 2.311 6.482 6.482 0 0 0 5.824.5a5.2 5.2 0 0 0-3.8 1.521c-1.915 1.916-2.315 5.392.625 8.333l7 7a.5.5 0 0 0 .708 0l7-7a6.6 6.6 0 0 0 2.123-4.508 5.179 5.179 0 0 0-1.533-3.793Z"
                                            />
                                        </svg>
                                        My likes
                                    </a>
                                </li>
                                <li>
                                    <a
                                        href="#"
                                        class="flex items-center px-4 py-2 text-sm hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white"
                                    >
                                        <svg
                                            class="w-4 h-4 mr-2 text-gray-400"
                                            aria-hidden="true"
                                            xmlns="http://www.w3.org/2000/svg"
                                            fill="currentColor"
                                            viewBox="0 0 20 20"
                                        >
                                            <path
                                                d="m1.56 6.245 8 3.924a1 1 0 0 0 .88 0l8-3.924a1 1 0 0 0 0-1.8l-8-3.925a1 1 0 0 0-.88 0l-8 3.925a1 1 0 0 0 0 1.8Z"
                                            />
                                            <path
                                                d="M18 8.376a1 1 0 0 0-1 1v.163l-7 3.434-7-3.434v-.163a1 1 0 0 0-2 0v.786a1 1 0 0 0 .56.9l8 3.925a1 1 0 0 0 .88 0l8-3.925a1 1 0 0 0 .56-.9v-.786a1 1 0 0 0-1-1Z"
                                            />
                                            <path
                                                d="M17.993 13.191a1 1 0 0 0-1 1v.163l-7 3.435-7-3.435v-.163a1 1 0 1 0-2 0v.787a1 1 0 0 0 .56.9l8 3.925a1 1 0 0 0 .88 0l8-3.925a1 1 0 0 0 .56-.9v-.787a1 1 0 0 0-1-1Z"
                                            />
                                        </svg>
                                        Collections
                                    </a>
                                </li>
                                <li>
                                    <a
                                        href="#"
                                        class="flex items-center justify-between px-4 py-2 text-sm hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white"
                                    >
                                        <span class="flex items-center">
                                            <svg
                                                class="w-4 h-4 mr-2 text-primary-600 dark:text-primary-500"
                                                aria-hidden="true"
                                                xmlns="http://www.w3.org/2000/svg"
                                                fill="currentColor"
                                                viewBox="0 0 20 20"
                                            >
                                                <path
                                                    d="m7.164 3.805-4.475.38L.327 6.546a1.114 1.114 0 0 0 .63 1.89l3.2.375 3.007-5.006ZM11.092 15.9l.472 3.14a1.114 1.114 0 0 0 1.89.63l2.36-2.362.38-4.475-5.102 3.067Zm8.617-14.283A1.613 1.613 0 0 0 18.383.291c-1.913-.33-5.811-.736-7.556 1.01-1.98 1.98-6.172 9.491-7.477 11.869a1.1 1.1 0 0 0 .193 1.316l.986.985.985.986a1.1 1.1 0 0 0 1.316.193c2.378-1.3 9.889-5.5 11.869-7.477 1.746-1.745 1.34-5.643 1.01-7.556Zm-3.873 6.268a2.63 2.63 0 1 1-3.72-3.72 2.63 2.63 0 0 1 3.72 3.72Z"
                                                />
                                            </svg>
                                            Pro version
                                        </span>
                                        <svg
                                            class="w-2.5 h-2.5 text-gray-400"
                                            aria-hidden="true"
                                            xmlns="http://www.w3.org/2000/svg"
                                            fill="none"
                                            viewBox="0 0 6 10"
                                        >
                                            <path
                                                stroke="currentColor"
                                                stroke-linecap="round"
                                                stroke-linejoin="round"
                                                stroke-width="2"
                                                d="m1 9 4-4-4-4"
                                            />
                                        </svg>
                                    </a>
                                </li>
                            </ul>
                            <ul
                                class="py-1 text-gray-500 dark:text-gray-400"
                                aria-labelledby="dropdown"
                            >
                                <li>
                                    <a
                                        href="#"
                                        class="block px-4 py-2 text-sm hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white"
                                        >Sign out</a
                                    >
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
            </nav>
        </header>

        <form class="max-w-md mx-auto mt-5">
            <div class="flex">
                <label
                    for="location-search"
                    class="mb-2 text-sm font-medium text-gray-900 sr-only dark:text-white"
                    >Your Email</label
                >
                <button
                    id="dropdown-button-2"
                    data-dropdown-toggle="dropdown-search-city"
                    class="flex-shrink-0 z-10 inline-flex items-center py-2.5 px-4 text-sm font-medium text-center text-gray-500 bg-gray-100 border border-gray-300 rounded-s-lg hover:bg-gray-200 focus:ring-4 focus:outline-none focus:ring-gray-100 dark:bg-gray-700 dark:hover:bg-gray-600 dark:focus:ring-gray-700 dark:text-white dark:border-gray-600"
                    type="button"
                >
                    All Category
                </button>
                <div
                    id="dropdown-search-city"
                    class="z-10 hidden bg-white divide-y divide-gray-100 rounded-lg shadow w-44 dark:bg-gray-700"
                >
                    <ul
                        class="py-2 text-sm text-gray-700 dark:text-gray-200"
                        aria-labelledby="dropdown-button-2"
                    >
                        <li>
                            <button
                                type="button"
                                class="inline-flex w-full px-4 py-2 text-sm text-gray-700 hover:bg-gray-100 dark:text-gray-200 dark:hover:bg-gray-600 dark:hover:text-white"
                                role="menuitem"
                            >
                                <div class="inline-flex items-center">
                                    United States
                                </div>
                            </button>
                        </li>
                    </ul>
                </div>
                <div class="relative w-full">
                    <input
                        type="search"
                        id="location-search"
                        class="block p-2.5 w-full z-20 text-sm text-gray-900 bg-gray-50 rounded-e-lg border-s-gray-50 border-s-2 border border-gray-300 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-s-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:border-blue-500"
                        placeholder="Search by category."
                        required
                    />
                    <button
                        type="submit"
                        class="absolute top-0 end-0 h-full p-2.5 text-sm font-medium text-white bg-blue-700 rounded-e-lg border border-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
                    >
                        <svg
                            class="w-4 h-4"
                            aria-hidden="true"
                            xmlns="http://www.w3.org/2000/svg"
                            fill="none"
                            viewBox="0 0 20 20"
                        >
                            <path
                                stroke="currentColor"
                                stroke-linecap="round"
                                stroke-linejoin="round"
                                stroke-width="2"
                                d="m19 19-4-4m0-7A7 7 0 1 1 1 8a7 7 0 0 1 14 0Z"
                            />
                        </svg>
                        <span class="sr-only">Search</span>
                    </button>
                </div>
            </div>
        </form>

        <div class="py-6 bg-white sm:py-8 lg:py-12">
            <div class="px-4 mx-auto max-w-screen-2xl md:px-8">
                <div class="flex items-end justify-between gap-4 mb-6">
                    <h2 class="text-2xl font-bold text-gray-800 lg:text-3xl">
                        Selected
                    </h2>

                    <a
                        href="#"
                        class="inline-block px-4 py-2 text-sm font-semibold text-center text-gray-500 transition duration-100 bg-white border rounded-lg outline-none ring-indigo-300 hover:bg-gray-100 focus-visible:ring active:bg-gray-200 md:px-8 md:py-3 md:text-base"
                        >Show more</a
                    >
                </div>

                <div
                    class="grid gap-x-4 gap-y-8 sm:grid-cols-2 md:gap-x-6 lg:grid-cols-3 xl:grid-cols-4"
                >
                    <!-- product - start -->
                    <div>
                        <a
                            href="#"
                            class="relative block mb-2 overflow-hidden bg-gray-100 rounded-lg group h-80 lg:mb-3"
                        >
                            <img
                                src="https://images.unsplash.com/photo-1523275335684-37898b6baf30?auto=format&q=75&fit=crop&w=600"
                                loading="lazy"
                                alt="Photo by Rachit Tank"
                                class="object-cover object-center w-full h-full transition duration-200 group-hover:scale-110"
                            />

                            <span
                                class="absolute left-0 top-0 rounded-br-lg bg-red-500 px-3 py-1.5 text-sm uppercase tracking-wider text-white"
                                >sale</span
                            >
                        </a>

                        <div>
                            <a
                                href="#"
                                class="mb-1 text-gray-500 transition duration-100 hover:gray-800 lg:text-lg"
                                >Timely Watch</a
                            >

                            <div class="flex items-end gap-2">
                                <span class="font-bold text-gray-800 lg:text-lg"
                                    >$15.00</span
                                >
                                <span class="mb-0.5 text-red-500 line-through"
                                    >$30.00</span
                                >
                            </div>
                        </div>
                    </div>
                    <!-- product - end -->

                    <!-- product - start -->
                    <div>
                        <a
                            href="#"
                            class="relative block mb-2 overflow-hidden bg-gray-100 rounded-lg group h-80 lg:mb-3"
                        >
                            <img
                                src="https://images.unsplash.com/photo-1485955900006-10f4d324d411?auto=format&q=75&fit=crop&w=600"
                                loading="lazy"
                                alt="Photo by Galina N"
                                class="object-cover object-center w-full h-full transition duration-200 group-hover:scale-110"
                            />
                        </a>

                        <div>
                            <a
                                href="#"
                                class="mb-1 text-gray-500 transition duration-100 hover:gray-800 lg:text-lg"
                                >Fancy Plant</a
                            >

                            <div class="flex items-end gap-2">
                                <span class="font-bold text-gray-800 lg:text-lg"
                                    >$9.00</span
                                >
                            </div>
                        </div>
                    </div>
                    <!-- product - end -->

                    <!-- product - start -->
                    <div>
                        <a
                            href="#"
                            class="relative block mb-2 overflow-hidden bg-gray-100 rounded-lg group h-80 lg:mb-3"
                        >
                            <img
                                src="https://images.unsplash.com/photo-1526170375885-4d8ecf77b99f?auto=format&q=75&fit=crop&w=600"
                                loading="lazy"
                                alt="Photo by eniko kis"
                                class="object-cover object-center w-full h-full transition duration-200 group-hover:scale-110"
                            />
                        </a>

                        <div>
                            <a
                                href="#"
                                class="mb-1 text-gray-500 transition duration-100 hover:gray-800 lg:text-lg"
                                >Elderly Cam</a
                            >

                            <div class="flex items-end gap-2">
                                <span class="font-bold text-gray-800 lg:text-lg"
                                    >$45.00</span
                                >
                            </div>
                        </div>
                    </div>
                    <!-- product - end -->

                    <!-- product - start -->
                    <div>
                        <a
                            href="#"
                            class="relative block mb-2 overflow-hidden bg-gray-100 rounded-lg group h-80 lg:mb-3"
                        >
                            <img
                                src="https://images.unsplash.com/photo-1560343090-f0409e92791a?auto=format&q=75&fit=crop&w=600"
                                loading="lazy"
                                alt="Photo by Irene Kredenets"
                                class="object-cover object-center w-full h-full transition duration-200 group-hover:scale-110"
                            />
                        </a>

                        <div>
                            <a
                                href="#"
                                class="mb-1 text-gray-500 transition duration-100 hover:gray-800 lg:text-lg"
                                >Shiny Shoe</a
                            >

                            <div class="flex items-end gap-2">
                                <span class="font-bold text-gray-800 lg:text-lg"
                                    >$29.00</span
                                >
                            </div>
                        </div>
                    </div>
                    <!-- product - end -->

                    <!-- product - start -->
                    <div>
                        <a
                            href="#"
                            class="relative block mb-2 overflow-hidden bg-gray-100 rounded-lg group h-80 lg:mb-3"
                        >
                            <img
                                src="https://images.unsplash.com/photo-1528476513691-07e6f563d97f?auto=format&q=75&fit=crop&w=600"
                                loading="lazy"
                                alt="Photo by Charles Deluvio"
                                class="object-cover object-center w-full h-full transition duration-200 group-hover:scale-110"
                            />
                        </a>

                        <div>
                            <a
                                href="#"
                                class="mb-1 text-gray-500 transition duration-100 hover:gray-800 lg:text-lg"
                                >Spiky Plant</a
                            >

                            <div class="flex items-end gap-2">
                                <span class="font-bold text-gray-800 lg:text-lg"
                                    >$4.00</span
                                >
                            </div>
                        </div>
                    </div>
                    <!-- product - end -->

                    <!-- product - start -->
                    <div>
                        <a
                            href="#"
                            class="relative block mb-2 overflow-hidden bg-gray-100 rounded-lg group h-80 lg:mb-3"
                        >
                            <img
                                src="https://images.unsplash.com/photo-1612033448550-9d6f9c17f07d?auto=format&q=75&fit=crop&w=600"
                                loading="lazy"
                                alt="Photo by Fernando Lavin"
                                class="object-cover object-center w-full h-full transition duration-200 group-hover:scale-110"
                            />
                        </a>

                        <div>
                            <a
                                href="#"
                                class="mb-1 text-gray-500 transition duration-100 hover:gray-800 lg:text-lg"
                                >Wieldy Film</a
                            >

                            <div class="flex items-end gap-2">
                                <span class="font-bold text-gray-800 lg:text-lg"
                                    >$19.00</span
                                >
                            </div>
                        </div>
                    </div>
                    <!-- product - end -->

                    <!-- product - start -->
                    <div>
                        <a
                            href="#"
                            class="relative block mb-2 overflow-hidden bg-gray-100 rounded-lg group h-80 lg:mb-3"
                        >
                            <img
                                src="https://images.unsplash.com/photo-1579609598065-79f8e5bcfb70?auto=format&q=75&fit=crop&w=600"
                                loading="lazy"
                                alt="Photo by Kiran CK"
                                class="object-cover object-center w-full h-full transition duration-200 group-hover:scale-110"
                            />
                            <span
                                class="absolute left-0 top-0 rounded-br-lg bg-red-500 px-3 py-1.5 text-sm uppercase tracking-wider text-white"
                                >sale</span
                            >
                        </a>

                        <div>
                            <a
                                href="#"
                                class="mb-1 text-gray-500 transition duration-100 hover:gray-800 lg:text-lg"
                                >Sturdy Stand</a
                            >

                            <div class="flex items-end gap-2">
                                <span class="font-bold text-gray-800 lg:text-lg"
                                    >$12.00</span
                                >
                                <span class="mb-0.5 text-red-500 line-through"
                                    >$24.00</span
                                >
                            </div>
                        </div>
                    </div>
                    <!-- product - end -->

                    <!-- product - start -->
                    <div>
                        <a
                            href="#"
                            class="relative block mb-2 overflow-hidden bg-gray-100 rounded-lg group h-80 lg:mb-3"
                        >
                            <img
                                src="https://images.unsplash.com/photo-1619066045029-5c7e8537bd8c?auto=format&q=75&fit=crop&w=600"
                                loading="lazy"
                                alt="Photo by Fakurian Design"
                                class="object-cover object-center w-full h-full transition duration-200 group-hover:scale-110"
                            />
                        </a>

                        <div>
                            <a
                                href="#"
                                class="mb-1 text-gray-500 transition duration-100 hover:gray-800 lg:text-lg"
                                >Lazy Bottle</a
                            >

                            <div class="flex items-end gap-2">
                                <span class="font-bold text-gray-800 lg:text-lg"
                                    >$9.00</span
                                >
                            </div>
                        </div>
                    </div>
                    <!-- product - end -->
                </div>
            </div>
        </div>

        <!-- footer -->

        <footer class="bg-white shadow dark:bg-gray-900">
            <div class="w-full max-w-screen-xl px-10 py-4 mx-auto md:py-8">
                <div class="sm:flex sm:items-center sm:justify-between">
                    <a
                        href="https://flowbite.com/"
                        class="flex items-center mb-4 space-x-3 sm:mb-0 rtl:space-x-reverse"
                    >
                        <img
                            src="https://flowbite.com/docs/images/logo.svg"
                            class="h-8"
                            alt="Flowbite Logo"
                        />
                        <span
                            class="self-center text-2xl font-semibold whitespace-nowrap dark:text-white"
                            >Flowbite</span
                        >
                    </a>
                    <ul
                        class="flex flex-wrap items-center mb-6 text-sm font-medium text-gray-500 sm:mb-0 dark:text-gray-400"
                    >
                        <li>
                            <a href="#" class="hover:underline me-4 md:me-6"
                                >About</a
                            >
                        </li>
                        <li>
                            <a href="#" class="hover:underline me-4 md:me-6"
                                >Privacy Policy</a
                            >
                        </li>
                        <li>
                            <a href="#" class="hover:underline me-4 md:me-6"
                                >Licensing</a
                            >
                        </li>
                        <li>
                            <a href="#" class="hover:underline">Contact</a>
                        </li>
                    </ul>
                </div>
                <hr
                    class="my-6 border-gray-200 sm:mx-auto dark:border-gray-700 lg:my-8"
                />
                <span
                    class="block text-sm text-gray-500 sm:text-center dark:text-gray-400"
                    >© 2023
                    <a href="https://flowbite.com/" class="hover:underline"
                        >Flowbite™</a
                    >. All Rights Reserved.</span
                >
            </div>
        </footer>
    </div>
</template>
