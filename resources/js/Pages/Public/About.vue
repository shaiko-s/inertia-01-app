<script setup>
import { ref } from 'vue'
const props = defineProps({
    count: Number,
    message: String,
})

const message = ref(props.message)

function reverseMessage() {
    // Access/mutate the value of a ref via
    // its .value property.
    message.value = message.value.split('').reverse().join('')
}

function notify() {
    alert('navigation was prevented.')
}

const isRed = ref(true)
const color = ref('green')

function toggleRed() {
    isRed.value = !isRed.value
}

function toggleColor() {
    color.value = color.value === 'green' ? 'blue' : 'green'
}

const show = ref(true)
const list = ref([1, 2, 3])
</script>

<template>
    <div class="container mx-auto my-8 px-4 flex bg-slate-300">
        <div class="w-3/4 mr-8 bg-green-300">
            <div class="flex items-center justify-between">
                <div class="flex flex-col items-center space-x-2 bg-gray-400">
                    <!--
    Bind to a method/function.
    The @click syntax is short for v-on:click.
  -->
                    <button @click="reverseMessage"
                            class=" border-2 border-green-600 px-3 py-2 rounded-lg mt-2 hover:bg-green-300 bg-green-500">Reverse
                        Message</button>

                    <!-- Can also be an inline expression statement -->
                    <button @click="message += '!'"
                            class=" border-2 border-green-600 px-3 py-2 rounded-lg mt-2 hover:bg-green-300 bg-green-500">Append
                        "!"</button>

                    <!--
  Vue also provides modifiers for common tasks
  such as e.preventDefault() and e.stopPropagation()
-->
                    <a href="https://vuejs.org"
                       @click.prevent="notify"
                       class=" text-blue-600 hover:text-blue-900 px-3 py-5">
                        A link with e.preventDefault()
                    </a>
                </div>
                <div class="flex items-center space-x-2 bg-gray-400">
                    two
                </div>
            </div>
        </div>
        <div class="w-1/4 bg-red-400 flex items-center">
            <h1 class="text-2xl font-semibold">{{ message }}</h1>
        </div>

    </div>

    <p>
        <span :title="message">
            Hover your mouse over me for a few seconds to see my dynamically bound title!
        </span>
    </p>

    <!--
  class bindings have special support for objects and arrays
  in addition to plain strings
  -->
    <p :class="{ red: isRed, blue: true }"
       @click="toggleRed">
        This should be red... but click me to toggle it. {{ isRed }}
    </p>

    <!-- style bindings also support object and arrays -->
    <p :style="{ color }"
       @click="toggleColor">
        This should be green, and should toggle between green and blue on click.
    </p>

    <div class="flex space-x-2 ml-2">
        <button @click="show = !show" class="border border-slate-700 rounded-md px-3 py-1">Toggle List</button>
        <button @click="list.push(list.length + 1)" class="border border-slate-700 rounded-md px-3 py-1">Push Number</button>
        <button @click="list.pop()" class="border border-slate-700 rounded-md px-3 py-1">Pop Number</button>
        <button @click="list.reverse()" class="border border-slate-700 rounded-md px-3 py-1">Reverse List</button>
    </div>

    <div class="ml-2 bg-slate-300 mt-5 ">
        <ul class="list-disc ml-4" v-if="show && list.length">
            <li class="" v-for="item of list">{{ item }}</li>
        </ul>
        <p v-else-if="list.length">List is not empty, but hidden.</p>
        <p v-else>List is empty.</p>
    </div>

</template>

<style>
.red {
    color: red;
}
</style>
