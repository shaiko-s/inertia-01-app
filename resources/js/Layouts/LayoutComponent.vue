<script setup>
import { Link } from '@inertiajs/vue3'
</script>

<template>
  <main class=" bg-lime-400">
    <header>
      <Link href="/">Home</Link>
      <Link href="/about">About</Link>
      <Link href="/contact">Contact</Link>
    </header>
    <article>
      <slot />
    </article>
  </main>
</template>
