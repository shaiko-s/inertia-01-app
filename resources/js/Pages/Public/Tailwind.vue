<script setup>
import { ref } from 'vue';
const count = ref(0);

const increment = () => {
    count.value++;
    console.log(count.value);
};
</script>

<template>
    <div class="p-4">
        <div class="flow-root ...">
            <div class="my-4 ...">Well, let me tell you something, ...</div>
        </div>
        <div class="flow-root ...">
            <div class="my-4 ...">Sure, go ahead, laugh if you want...</div>
        </div>
    </div>

    <!-- <div class="text-gray-900 text-sm">
        <nav class="bg-gray-900 text-white px-4 py-3 flex items-center justify-between">
            <div class="flex items-center space-x-4">
                <a href="#"
                   class="text-white hover:text-gray-400">
                    <svg aria-hidden="true"
                         viewBox="0 0 24 24"
                         data-view-component="true"
                         class="w-8 fill-current">
                        <path
                              d="M12.5.75C6.146.75 1 5.896 1 12.25c0 5.089 3.292 9.387 7.863 10.91.575.101.79-.244.79-.546 0-.273-.014-1.178-.014-2.142-2.889.532-3.636-.704-3.866-1.35-.13-.331-.69-1.352-1.18-1.625-.402-.216-.977-.748-.014-.762.906-.014 1.553.834 1.769 1.179 1.035 1.74 2.688 1.25 3.349.948.1-.747.402-1.25.733-1.538-2.559-.287-5.232-1.279-5.232-5.678 0-1.25.445-2.285 1.178-3.09-.115-.288-.517-1.467.115-3.048 0 0 .963-.302 3.163 1.179.92-.259 1.897-.388 2.875-.388.977 0 1.955.13 2.875.388 2.2-1.495 3.162-1.179 3.162-1.179.633 1.581.23 2.76.115 3.048.733.805 1.179 1.825 1.179 3.09 0 4.413-2.688 5.39-5.247 5.678.417.36.776 1.05.776 2.128 0 1.538-.014 2.774-.014 3.162 0 .302.216.662.79.547C20.709 21.637 24 17.324 24 12.25 24 5.896 18.854.75 12.5.75Z">
                        </path>
                    </svg>
                </a>
                <div class="relative">
                    <input type="text"
                           class="rounded bg-gray-700 placeholder-white w-72 px-3 py-1"
                           placeholder="Search or jump to...">
                    <div class="absolute top-0 right-0 flex items-center h-full">
                        <div class="border border-gray-600 rounded text-xs text-gray-400 px-2 mr-2">/</div>
                    </div>
                </div>
                <ul class="flex items-center font-semibold space-x-4">
                    <li><a href="#"
                           class="hover:text-gray-400">Pull Requests</a></li>
                    <li><a href="#"
                           class="hover:text-gray-400">Issues</a></li>
                    <li><a href="#"
                           class="hover:text-gray-400">Marketplace</a></li>
                    <li><a href="#"
                           class="hover:text-gray-400">Explore</a></li>
                </ul>
            </div>
            <div class="flex items-center space-x-4 text-white">
                <a href="#"
                   class="relative hover:text-gray-400">
                    <svg class="w-5"
                         data-slot="icon"
                         fill="none"
                         stroke-width="1.5"
                         stroke="currentColor"
                         viewBox="0 0 24 24"
                         xmlns="http://www.w3.org/2000/svg"
                         aria-hidden="true">
                        <path stroke-linecap="round"
                              stroke-linejoin="round"
                              d="M14.857 17.082a23.848 23.848 0 0 0 5.454-1.31A8.967 8.967 0 0 1 18 9.75V9A6 6 0 0 0 6 9v.75a8.967 8.967 0 0 1-2.312 6.022c1.733.64 3.56 1.085 5.455 1.31m5.714 0a24.255 24.255 0 0 1-5.714 0m5.714 0a3 3 0 1 1-5.714 0">
                        </path>
                    </svg>
                    <div class="bg-blue-600 rounded-full w-2 h-2 absolute top-0 right-0"></div>
                </a>
                <a href="#"
                   class="flex items-center hover:text-gray-400">
                    <svg class="w-5"
                         data-slot="icon"
                         fill="none"
                         stroke-width="1.5"
                         stroke="currentColor"
                         viewBox="0 0 24 24"
                         xmlns="http://www.w3.org/2000/svg"
                         aria-hidden="true">
                        <path stroke-linecap="round"
                              stroke-linejoin="round"
                              d="M12 4.5v15m7.5-7.5h-15"></path>
                    </svg>
                    <svg class="w-3 ml-1"
                         data-slot="icon"
                         fill="none"
                         stroke-width="1.5"
                         stroke="currentColor"
                         viewBox="0 0 24 24"
                         xmlns="http://www.w3.org/2000/svg"
                         aria-hidden="true">
                        <path stroke-linecap="round"
                              stroke-linejoin="round"
                              d="m19.5 8.25-7.5 7.5-7.5-7.5"></path>
                    </svg>
                </a>
                <a href="#"
                   class="flex items-center hover:text-gray-400">
                    <img src="https://avatars.githubusercontent.com/u/145833407?v=4"
                         alt=""
                         size="32"
                         height="32"
                         width="32"
                         data-view-component="true"
                         class="w-5 h-5 rounded-full">
                    <svg class="w-3 ml-1"
                         data-slot="icon"
                         fill="none"
                         stroke-width="1.5"
                         stroke="currentColor"
                         viewBox="0 0 24 24"
                         xmlns="http://www.w3.org/2000/svg"
                         aria-hidden="true">
                        <path stroke-linecap="round"
                              stroke-linejoin="round"
                              d="m19.5 8.25-7.5 7.5-7.5-7.5"></path>
                    </svg>
                </a>
            </div>
        </nav>
    </div>
    <div class="relative bg-indigo-600 text-white size-96">
        <h2>Relative</h2>
        <div class="absolute right-12 bottom-6 bg-green-600">Absolute</div>
    </div>
    <div class="sticky top-0 left-0 bg-indigo-500 text-white">A</div>
    <div class="h-screen bg-indigo-200"></div>
    <div class="sticky top-0 left-0 bg-indigo-500 text-white">B</div>
    <div class="h-screen bg-indigo-300"></div>
    <div class="sticky top-0 left-0 bg-indigo-500 text-white">C</div>
    <div class="h-screen bg-indigo-400"></div>
    <div class="relative flex min-h-screen flex-col justify-center overflow-hidden bg-gray-50 py-6 sm:py-12">

        <div
             class="absolute inset-0 bg-[url(/img/grid.svg)] bg-center [mask-image:linear-gradient(180deg,white,rgba(255,255,255,0))]">
        </div>
        <div
             class="relative bg-white px-6 pt-10 pb-8 shadow-xl ring-1 ring-gray-900/5 sm:mx-auto sm:max-w-lg sm:rounded-lg sm:px-10">
            <div class="mx-auto max-w-md">
                <img src="/../img/logo.svg"
                     class="h-6"
                     alt="Tailwind Play" />
                <div class="divide-y divide-gray-300/50">
                    <div class="space-y-6 py-8 text-base leading-7 text-gray-600">

                    </div>
                    <div class="">
                        <p class="text-gray-900">Want to dig deeper into Tailwind?</p>
                        <p>
                            <a href="https://tailwindcss.com/docs"
                               class="text-sky-500 hover:text-sky-600">Read the docs &rarr;</a>
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </div> -->
</template>
