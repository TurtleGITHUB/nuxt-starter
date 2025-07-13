<template>
  <div id="app">
    <AppHeader />
    <main class="main-content">
      <NuxtPage />
    </main>
    <AppFooter />
  </div>
</template>

<script setup>
useHead({
  titleTemplate: '%s - D&D Adventures',
  meta: [
    { name: 'description', content: 'Your ultimate guide to Dungeons & Dragons adventures, tips, and resources' },
    { name: 'viewport', content: 'width=device-width, initial-scale=1' },
    { charset: 'utf-8' }
  ],
  link: [
    { rel: 'icon', type: 'image/x-icon', href: '/favicon.ico' },
    { rel: 'preconnect', href: 'https://fonts.googleapis.com' },
    { rel: 'preconnect', href: 'https://fonts.gstatic.com', crossorigin: '' },
    { rel: 'stylesheet', href: 'https://fonts.googleapis.com/css2?family=Cinzel:wght@400;500;600;700&family=Open+Sans:wght@300;400;500;600;700&display=swap' }
  ]
})
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

:root {
  --primary-color: #8B4513;
  --secondary-color: #D2691E;
  --accent-color: #FFD700;
  --text-color: #2C1810;
  --text-light: #5D4037;
  --background: #FFF8E1;
  --card-bg: #FFFFFF;
  --border-color: #D7CCC8;
  --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  --shadow-hover: 0 8px 15px rgba(0, 0, 0, 0.2);
}

body {
  font-family: 'Open Sans', sans-serif;
  line-height: 1.6;
  color: var(--text-color);
  background-color: var(--background);
  background-image: 
    radial-gradient(circle at 20% 80%, rgba(139, 69, 19, 0.1) 0%, transparent 50%),
    radial-gradient(circle at 80% 20%, rgba(210, 105, 30, 0.1) 0%, transparent 50%);
  min-height: 100vh;
}

#app {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.main-content {
  flex: 1;
  padding: 2rem 0;
}

h1, h2, h3, h4, h5, h6 {
  font-family: 'Cinzel', serif;
  font-weight: 600;
  line-height: 1.2;
  margin-bottom: 1rem;
}

h1 {
  font-size: 2.5rem;
  color: var(--primary-color);
}

h2 {
  font-size: 2rem;
  color: var(--primary-color);
}

h3 {
  font-size: 1.5rem;
  color: var(--text-color);
}

p {
  margin-bottom: 1rem;
  color: var(--text-light);
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.btn {
  display: inline-block;
  padding: 0.75rem 1.5rem;
  background: var(--primary-color);
  color: white;
  text-decoration: none;
  border-radius: 0.5rem;
  font-weight: 500;
  transition: all 0.3s ease;
  border: none;
  cursor: pointer;
  font-family: 'Open Sans', sans-serif;
}

.btn:hover {
  background: var(--secondary-color);
  transform: translateY(-2px);
  box-shadow: var(--shadow-hover);
}

.btn-secondary {
  background: var(--secondary-color);
  color: white;
}

.btn-secondary:hover {
  background: var(--primary-color);
}

.btn-outline {
  background: transparent;
  color: var(--primary-color);
  border: 2px solid var(--primary-color);
}

.btn-outline:hover {
  background: var(--primary-color);
  color: white;
}

.card {
  background: var(--card-bg);
  border-radius: 1rem;
  padding: 2rem;
  box-shadow: var(--shadow);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  border: 1px solid var(--border-color);
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: var(--shadow-hover);
}

.dice-icon {
  color: var(--accent-color);
  font-size: 1.5rem;
  margin-right: 0.5rem;
}

@media (max-width: 768px) {
  .container {
    padding: 0 1rem;
  }
  
  h1 {
    font-size: 2rem;
  }
  
  h2 {
    font-size: 1.5rem;
  }
  
  .main-content {
    padding: 1rem 0;
  }
}
</style>
