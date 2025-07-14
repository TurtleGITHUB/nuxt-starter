<template>
  <section class="container mx-auto py-12">
    <h1 class="text-4xl font-bold mb-4">Contact Us</h1>
    <p class="text-lg text-gray-700 mb-6">
      Have questions or feedback? Fill out the form below to get in touch!
    </p>
    <form class="max-w-lg space-y-4">
      <div>
        <label class="block text-gray-700 mb-1">Name</label>
        <input type="text" class="w-full border rounded px-3 py-2" placeholder="Your Name" />
      </div>
      <div>
        <label class="block text-gray-700 mb-1">Email</label>
        <input type="email" class="w-full border rounded px-3 py-2" placeholder="you@example.com" />
      </div>
      <div>
        <label class="block text-gray-700 mb-1">Message</label>
        <textarea class="w-full border rounded px-3 py-2" rows="4" placeholder="Your message"></textarea>
      </div>
      <button type="submit" class="bg-blue-600 text-white px-4 py-2 rounded">Send</button>
    </form>
  </section>
</template>

<script setup>
// Add form handling logic here if desired
</script>
