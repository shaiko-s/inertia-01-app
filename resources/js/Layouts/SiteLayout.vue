<script setup>
import { Link } from '@inertiajs/vue3'
</script>

<template>
    <header class="bg-yellow-200">

        <h1>Default Header</h1>

    </header>

    <div class="container bg-gray-200">


            <slot class="flex" />

    </div>
</template>
