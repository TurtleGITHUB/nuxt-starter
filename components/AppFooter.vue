<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-content">
        <div class="footer-section">
          <h3>D&D Adventures</h3>
          <p>Your ultimate guide to Dungeons & Dragons adventures, tips, and resources for players and dungeon masters alike.</p>
          <div class="social-links">
            <a href="#" aria-label="Twitter"><span class="icon">🐦</span></a>
            <a href="#" aria-label="Discord"><span class="icon">💬</span></a>
            <a href="#" aria-label="YouTube"><span class="icon">📺</span></a>
          </div>
        </div>
        
        <div class="footer-section">
          <h4>Quick Links</h4>
          <ul>
            <li><NuxtLink to="/">Home</NuxtLink></li>
            <li><NuxtLink to="/about">About</NuxtLink></li>
            <li><NuxtLink to="/blog">Blog</NuxtLink></li>
            <li><NuxtLink to="/contact">Contact</NuxtLink></li>
          </ul>
        </div>
        
        <div class="footer-section">
          <h4>Resources</h4>
          <ul>
            <li><a href="#" target="_blank">D&D Beyond</a></li>
            <li><a href="#" target="_blank">Roll20</a></li>
            <li><a href="#" target="_blank">Dungeon Master's Guide</a></li>
            <li><a href="#" target="_blank">Player's Handbook</a></li>
          </ul>
        </div>
        
        <div class="footer-section">
          <h4>Newsletter</h4>
          <p>Stay updated with the latest adventures and tips!</p>
          <form @submit.prevent="subscribeNewsletter" class="newsletter-form">
            <input 
              type="email" 
              placeholder="Enter your email" 
              v-model="email"
              required
            >
            <button type="submit" class="btn btn-secondary">Subscribe</button>
          </form>
        </div>
      </div>
      
      <div class="footer-bottom">
        <p>&copy; {{ currentYear }} D&D Adventures. All rights reserved.</p>
        <p class="disclaimer">
          Dungeons & Dragons is a trademark of Wizards of the Coast LLC. 
          This site is not affiliated with Wizards of the Coast.
        </p>
      </div>
    </div>
  </footer>
</template>

<script setup>
import { ref, computed } from 'vue'

const email = ref('')
const currentYear = computed(() => new Date().getFullYear())

const subscribeNewsletter = () => {
  // Handle newsletter subscription
  alert(`Thank you for subscribing with email: ${email.value}`)
  email.value = ''
}
</script>

<style scoped>
.footer {
  background: linear-gradient(135deg, var(--text-color) 0%, var(--primary-color) 100%);
  color: white;
  padding: 3rem 0 1rem;
  margin-top: auto;
}

.footer-content {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
  margin-bottom: 2rem;
}

.footer-section h3 {
  font-family: 'Cinzel', serif;
  color: var(--accent-color);
  margin-bottom: 1rem;
  font-size: 1.5rem;
}

.footer-section h4 {
  color: var(--accent-color);
  margin-bottom: 1rem;
  font-size: 1.2rem;
}

.footer-section p {
  color: rgba(255, 255, 255, 0.8);
  line-height: 1.6;
  margin-bottom: 1rem;
}

.footer-section ul {
  list-style: none;
  padding: 0;
}

.footer-section ul li {
  margin-bottom: 0.5rem;
}

.footer-section ul li a {
  color: rgba(255, 255, 255, 0.8);
  text-decoration: none;
  transition: color 0.3s ease;
}

.footer-section ul li a:hover {
  color: var(--accent-color);
}

.social-links {
  display: flex;
  gap: 1rem;
  margin-top: 1rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  background: rgba(255, 255, 255, 0.1);
  border-radius: 50%;
  text-decoration: none;
  transition: all 0.3s ease;
}

.social-links a:hover {
  background: var(--accent-color);
  transform: translateY(-2px);
}

.social-links .icon {
  font-size: 1.2rem;
}

.newsletter-form {
  display: flex;
  gap: 0.5rem;
  margin-top: 1rem;
}

.newsletter-form input {
  flex: 1;
  padding: 0.75rem;
  border: none;
  border-radius: 0.5rem;
  font-size: 1rem;
  background: rgba(255, 255, 255, 0.1);
  color: white;
  border: 1px solid rgba(255, 255, 255, 0.3);
}

.newsletter-form input::placeholder {
  color: rgba(255, 255, 255, 0.6);
}

.newsletter-form input:focus {
  outline: none;
  border-color: var(--accent-color);
  background: rgba(255, 255, 255, 0.2);
}

.newsletter-form button {
  padding: 0.75rem 1rem;
  white-space: nowrap;
}

.footer-bottom {
  text-align: center;
  padding-top: 2rem;
  border-top: 1px solid rgba(255, 255, 255, 0.2);
  color: rgba(255, 255, 255, 0.6);
}

.disclaimer {
  font-size: 0.9rem;
  margin-top: 0.5rem;
  font-style: italic;
}

@media (max-width: 768px) {
  .footer-content {
    grid-template-columns: 1fr;
    gap: 2rem;
  }
  
  .newsletter-form {
    flex-direction: column;
  }
  
  .newsletter-form button {
    align-self: flex-start;
  }
  
  .social-links {
    justify-content: center;
  }
}
</style>
