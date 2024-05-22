<script setup></script>

<template>
    <header class="mb-8 bg-gray-800 -z-0">
        <div
            class="flex flex-wrap items-center justify-between px-4 mx-auto max-w-screen-2xl md:px-10"
        >
            <!-- logo - start -->
            <a
                href="/"
                class="inline-flex items-center gap-2.5 text-xl font-bold text-white md:text-3xl"
                aria-label="logo"
            >
                <img
                    src="https://github.com/sa-sa-creator/Images/blob/main/RanyLogo.png?raw=true"
                    class="w-14"
                    alt=""
                />

                Rany Shop
            </a>
            <div class="hidden w-4/12 md:inline-block">
                <form class="max-w-md mx-auto">
                    <div class="relative">
                        <input
                            type="search"
                            id="default-search"
                            class="w-full h-10 p-2 text-sm text-gray-900 border border-gray-300 rounded-lg ablock bg-gray-50 focus:ring-yellow-500 focus:border-yellow-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-yellow-500 dark:focus:border-yellow-500"
                            placeholder="Search product..."
                            required
                        />
                        <button
                            type="submit"
                            class="absolute px-4 py-2 text-sm font-medium text-white rounded-lg end-1 bottom-1 hover:bg-gray-200 focus:ring-4 focus:outline-none focus:ring-yellow-300 dark:bg-gray-200 dark:hover:bg-gray-200 dark:focus:ring-yellow-500"
                        >
                            <svg
                                class="w-4 h-4 text-gray-500 dark:text-gray-400"
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
                    </div>
                </form>
            </div>

            <div class="flex gap-0 lg:flex 2xl:ml-16">
                <button
                    type="button"
                    id="user-menu-button"
                    aria-expanded="false"
                    data-dropdown-toggle="user-dropdown"
                    data-dropdown-placement="bottom"
                ></button>
                <a
                    href="#"
                    class="flex h-12 w-12 flex-col items-center justify-center gap-1.5 transition duration-100 hover:bg-gray-500 active:bg-gray-200 sm:h-20 sm:w-20 md:h-24 md:w-24"
                >
                    <svg
                        xmlns="http://www.w3.org/2000/svg"
                        class="w-6 h-6 text-white"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke="currentColor"
                    >
                        <path
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            stroke-width="2"
                            d="M16 11V7a4 4 0 00-8 0v4M5 9h14l1 12H4L5 9z"
                        />
                    </svg>
                    <div
                        class="absolute inline-flex items-center justify-center w-auto px-1 text-xs font-bold text-white bg-red-500 border-2 border-red-500 rounded-full lg:top-6 lg:end-40 dark:border-gray-900 2xl:end-auto"
                    >
                        0
                    </div>

                    <span
                        class="hidden text-xs font-semibold text-white sm:block"
                        >Cart</span
                    >
                </a>
                <button
                    id="user-menu-button"
                    aria-expanded="false"
                    data-dropdown-toggle="user-dropdown"
                    data-dropdown-placement="bottom"
                    class="flex h-12 w-12 flex-col items-center justify-center gap-1.5 transition duration-100 hover:bg-gray-500 active:bg-gray-200 sm:h-20 sm:w-20 md:h-24 md:w-24"
                >
                    <svg
                        xmlns="http://www.w3.org/2000/svg"
                        class="w-6 h-6 text-white"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke="currentColor"
                    >
                        <path
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            stroke-width="2"
                            d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z"
                        />
                    </svg>

                    <span
                        class="hidden text-xs font-semibold text-white sm:block"
                        >Account</span
                    >
                </button>
                <!-- Dropdown menu -->
                <div
                    class="z-50 hidden my-4 text-base list-none divide-y divide-gray-100 rounded-lg shadow bg-slate-100 dark:bg-gray-700 dark:divide-gray-600"
                    id="user-dropdown"
                >
                    <div class="px-4 py-3">
                        <span
                            class="block text-sm text-gray-900 dark:text-white"
                            >Bonnie Green</span
                        >
                        <span
                            class="block text-sm text-gray-500 truncate dark:text-gray-400"
                            >name@flowbite.com</span
                        >
                    </div>
                    <ul class="py-2" aria-labelledby="user-menu-button">
                        <li>
                            <a
                                href="#"
                                class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-200 dark:hover:bg-gray-600 dark:text-gray-200 dark:hover:text-white"
                                >Profile</a
                            >
                        </li>
                        <li>
                            <a
                                href="#"
                                class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-200 dark:hover:bg-gray-600 dark:text-gray-200 dark:hover:text-white"
                                >History</a
                            >
                        </li>
                        <li>
                            <a
                                href="#"
                                class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-200 dark:hover:bg-gray-600 dark:text-gray-200 dark:hover:text-white"
                                >Earnings</a
                            >
                        </li>
                        <li>
                            <a
                                href="#"
                                class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-200 dark:hover:bg-gray-600 dark:text-gray-200 dark:hover:text-white"
                                >Sign out</a
                            >
                        </li>
                    </ul>
                </div>
            </div>

            <!-- buttons - end -->
        </div>
    </header>
</template>
