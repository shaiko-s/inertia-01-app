<script setup>
import SiteLayout from '@/Layouts/SiteLayout.vue';
import NestedLayout from '@/Layouts/NestedLayout.vue';
import { Head } from '@inertiajs/vue3'

defineProps({ user: Object })

// defineOptions({
//     layout: [SiteLayout, NestedLayout],
// })
</script>

<template>

    <Head title="Welcome" />

    <h1>Welcome</h1>
    <p>Hello {{ user.name ?? 'guest' }}, welcome to your first Inertia app!</p>

    <div class="columns-2">
        <p>Well, let me tell you something, ...</p>
        <p class="break-after-column">Sure, go ahead, laugh...</p>
        <p>Maybe we can live without...</p>
        <p>Look. If you think this is...</p>
    </div>

</template>
