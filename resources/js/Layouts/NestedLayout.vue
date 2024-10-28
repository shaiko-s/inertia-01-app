<script setup>
import { Link } from '@inertiajs/vue3'
</script>

<template>


      <nav class="bg-green-200">
          <Link href="/">Nested</Link>
          <Link href="/about">Lay</Link>
          <Link href="/contact">out</Link>
      </nav>

    <main class="bg-red-200">
      <slot />
    </main>

</template>
