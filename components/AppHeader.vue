<template>
  <header class="header">
    <div class="container">
      <nav class="nav">
        <NuxtLink to="/" class="logo">
          <span class="dice-icon">🎲</span>
          D&D Adventures
        </NuxtLink>
        
        <button class="mobile-menu-toggle" @click="toggleMobileMenu" aria-label="Toggle menu">
          <span class="hamburger"></span>
        </button>
        
        <ul class="nav-links" :class="{ 'nav-links-open': mobileMenuOpen }">
          <li><NuxtLink to="/" @click="closeMobileMenu">Home</NuxtLink></li>
          <li><NuxtLink to="/about" @click="closeMobileMenu">About</NuxtLink></li>
          <li><NuxtLink to="/blog" @click="closeMobileMenu">Blog</NuxtLink></li>
          <li><NuxtLink to="/contact" @click="closeMobileMenu">Contact</NuxtLink></li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue'

const mobileMenuOpen = ref(false)

const toggleMobileMenu = () => {
  mobileMenuOpen.value = !mobileMenuOpen.value
}

const closeMobileMenu = () => {
  mobileMenuOpen.value = false
}
</script>

<style scoped>
.header {
  background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  position: sticky;
  top: 0;
  z-index: 1000;
}

.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 0;
}

.logo {
  font-family: 'Cinzel', serif;
  font-size: 1.8rem;
  font-weight: 700;
  color: white;
  text-decoration: none;
  display: flex;
  align-items: center;
  transition: color 0.3s ease;
}

.logo:hover {
  color: var(--accent-color);
}

.dice-icon {
  font-size: 2rem;
  margin-right: 0.5rem;
  animation: roll 2s infinite;
}

@keyframes roll {
  0%, 90%, 100% { transform: rotate(0deg); }
  10% { transform: rotate(90deg); }
  20% { transform: rotate(180deg); }
  30% { transform: rotate(270deg); }
  40% { transform: rotate(360deg); }
}

.mobile-menu-toggle {
  display: none;
  background: none;
  border: none;
  cursor: pointer;
  padding: 0.5rem;
  position: relative;
  z-index: 1001;
}

.hamburger {
  display: block;
  width: 25px;
  height: 3px;
  background: white;
  position: relative;
  transition: all 0.3s ease;
}

.hamburger::before,
.hamburger::after {
  content: '';
  position: absolute;
  width: 25px;
  height: 3px;
  background: white;
  transition: all 0.3s ease;
}

.hamburger::before {
  top: -8px;
}

.hamburger::after {
  bottom: -8px;
}

.nav-links {
  display: flex;
  list-style: none;
  gap: 2rem;
  margin: 0;
  padding: 0;
}

.nav-links a {
  color: white;
  text-decoration: none;
  font-weight: 500;
  padding: 0.5rem 1rem;
  border-radius: 0.5rem;
  transition: all 0.3s ease;
  position: relative;
}

.nav-links a:hover {
  background: rgba(255, 255, 255, 0.1);
  color: var(--accent-color);
}

.nav-links a.router-link-active {
  background: rgba(255, 255, 255, 0.2);
  color: var(--accent-color);
}

@media (max-width: 768px) {
  .mobile-menu-toggle {
    display: block;
  }
  
  .nav-links {
    position: absolute;
    top: 100%;
    left: 0;
    right: 0;
    background: var(--primary-color);
    flex-direction: column;
    padding: 1rem 0;
    gap: 0;
    transform: translateY(-100%);
    opacity: 0;
    visibility: hidden;
    transition: all 0.3s ease;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }
  
  .nav-links-open {
    transform: translateY(0);
    opacity: 1;
    visibility: visible;
  }
  
  .nav-links li {
    margin: 0;
  }
  
  .nav-links a {
    display: block;
    padding: 1rem 2rem;
    border-radius: 0;
  }
  
  .nav-links a:hover {
    background: rgba(255, 255, 255, 0.1);
    padding-left: 2.5rem;
  }
}
</style>
