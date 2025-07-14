<template>
  <section class="container mx-auto py-12">
    <h1 class="text-4xl font-bold mb-4">Blog</h1>
    <p class="text-lg text-gray-700 mb-6">
      Read our latest articles and updates below.
    </p>
    <!-- Example static blog list; replace with dynamic as needed -->
    <ul>
      <li class="mb-2">
        <NuxtLink to="/blog/lost-mines-guide" class="text-blue-600 hover:underline">Lost Mines Guide</NuxtLink>
      </li>
      <li class="mb-2">
        <NuxtLink to="/blog/memorable-npcs" class="text-blue-600 hover:underline">Memorable NPCs</NuxtLink>
      </li>
      <li class="mb-2">
        <NuxtLink to="/blog/combat-tips" class="text-blue-600 hover:underline">Combat Tips</NuxtLink>
      </li>
    </ul>
  </section>
</template>

<script setup>
// Use composables to fetch posts if needed in the future
</script>
