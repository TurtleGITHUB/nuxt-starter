<template>
  <div>
    <!-- Hero Section -->
    <section class="hero">
      <div class="container">
        <div class="hero-content">
          <h1 class="hero-title">
            <span class="dice-icon">🎲</span>
            Welcome to D&D Adventures
          </h1>
          <p class="hero-subtitle">
            Embark on epic quests, master the art of storytelling, and discover the magic of Dungeons & Dragons
          </p>
          <div class="hero-buttons">
            <NuxtLink to="/about" class="btn btn-primary">Start Your Journey</NuxtLink>
            <NuxtLink to="/blog" class="btn btn-outline">Read Adventures</NuxtLink>
          </div>
        </div>
        <div class="hero-image">
          <div class="dice-container">
            <div class="dice d20">20</div>
            <div class="dice d12">12</div>
            <div class="dice d10">10</div>
            <div class="dice d8">8</div>
            <div class="dice d6">6</div>
            <div class="dice d4">4</div>
          </div>
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section class="features">
      <div class="container">
        <h2 class="section-title">What Awaits You</h2>
        <div class="features-grid">
          <div class="feature-card card">
            <div class="feature-icon">⚔️</div>
            <h3>Epic Adventures</h3>
            <p>Discover thrilling campaigns and one-shots that will challenge your party and create unforgettable memories.</p>
          </div>
          
          <div class="feature-card card">
            <div class="feature-icon">📚</div>
            <h3>DM Resources</h3>
            <p>Comprehensive guides, tools, and tips to help you become the best Dungeon Master your table has ever seen.</p>
          </div>
          
          <div class="feature-card card">
            <div class="feature-icon">🎭</div>
            <h3>Character Building</h3>
            <p>Master the art of character creation with detailed guides on races, classes, and roleplay techniques.</p>
          </div>
          
          <div class="feature-card card">
            <div class="feature-icon">🗺️</div>
            <h3>World Building</h3>
            <p>Learn to craft immersive worlds filled with rich lore, compelling NPCs, and endless possibilities.</p>
          </div>
          
          <div class="feature-card card">
            <div class="feature-icon">🎲</div>
            <h3>Rules & Mechanics</h3>
            <p>Clear explanations of game mechanics, house rules, and tips for smooth gameplay sessions.</p>
          </div>
          
          <div class="feature-card card">
            <div class="feature-icon">👥</div>
            <h3>Community</h3>
            <p>Connect with fellow adventurers, share stories, and find groups to embark on new quests together.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Recent Blog Posts -->
    <section class="recent-posts">
      <div class="container">
        <h2 class="section-title">Recent Adventures</h2>
        <div class="posts-grid">
          <article class="post-preview card">
            <div class="post-category">Campaign Guide</div>
            <h3>The Lost Mines of Phandelver: A Beginner's Guide</h3>
            <p>Everything you need to know to run this classic starter adventure, including tips for new DMs and common pitfalls to avoid.</p>
            <div class="post-meta">
              <span class="post-date">🗓️ March 15, 2024</span>
              <span class="post-read-time">📖 8 min read</span>
            </div>
            <NuxtLink to="/blog/lost-mines-guide" class="read-more">Continue Reading →</NuxtLink>
          </article>
          
          <article class="post-preview card">
            <div class="post-category">Character Creation</div>
            <h3>Building Memorable NPCs That Players Will Love</h3>
            <p>Learn the secrets of creating non-player characters that feel real, have clear motivations, and drive your story forward.</p>
            <div class="post-meta">
              <span class="post-date">🗓️ March 10, 2024</span>
              <span class="post-read-time">📖 12 min read</span>
            </div>
            <NuxtLink to="/blog/memorable-npcs" class="read-more">Continue Reading →</NuxtLink>
          </article>
          
          <article class="post-preview card">
            <div class="post-category">DM Tips</div>
            <h3>Running Combat: How to Keep It Fast and Fun</h3>
            <p>Practical strategies for managing combat encounters that keep your players engaged and the story moving forward.</p>
            <div class="post-meta">
              <span class="post-date">🗓️ March 5, 2024</span>
              <span class="post-read-time">📖 6 min read</span>
            </div>
            <NuxtLink to="/blog/combat-tips" class="read-more">Continue Reading →</NuxtLink>
          </article>
        </div>
        
        <div class="view-all">
          <NuxtLink to="/blog" class="btn btn-secondary">View All Posts</NuxtLink>
        </div>
      </div>
    </section>

    <!-- Call to Action -->
    <section class="cta">
      <div class="container">
        <div class="cta-content">
          <h2>Ready to Begin Your Adventure?</h2>
          <p>Join thousands of adventurers who have discovered the magic of D&D through our guides and resources.</p>
          <NuxtLink to="/contact" class="btn btn-primary">Get Started Today</NuxtLink>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
useHead({
  title: 'Home',
  meta: [
    { name: 'description', content: 'Welcome to D&D Adventures - Your ultimate guide to Dungeons & Dragons with campaigns, character guides, and DM resources.' }
  ]
})
</script>

<style scoped>
.hero {
  background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
  color: white;
  padding: 4rem 0;
  margin-bottom: 4rem;
}

.hero .container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 3rem;
  align-items: center;
}

.hero-title {
  font-size: 3.5rem;
  margin-bottom: 1rem;
  color: white;
  display: flex;
  align-items: center;
  gap: 1rem;
}

.hero-title .dice-icon {
  font-size: 3rem;
  animation: bounce 2s infinite;
}

@keyframes bounce {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-10px); }
}

.hero-subtitle {
  font-size: 1.3rem;
  margin-bottom: 2rem;
  opacity: 0.9;
  line-height: 1.6;
}

.hero-buttons {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
}

.hero-image {
  display: flex;
  justify-content: center;
  align-items: center;
}

.dice-container {
  position: relative;
  width: 300px;
  height: 300px;
}

.dice {
  position: absolute;
  width: 60px;
  height: 60px;
  background: var(--accent-color);
  color: var(--text-color);
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
  font-size: 1.2rem;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
  animation: float 3s ease-in-out infinite;
}

.dice.d20 { top: 20px; left: 120px; animation-delay: 0s; }
.dice.d12 { top: 80px; right: 50px; animation-delay: 0.5s; }
.dice.d10 { bottom: 80px; right: 80px; animation-delay: 1s; }
.dice.d8 { bottom: 60px; left: 60px; animation-delay: 1.5s; }
.dice.d6 { top: 120px; left: 20px; animation-delay: 2s; }
.dice.d4 { top: 60px; right: 120px; animation-delay: 2.5s; }

@keyframes float {
  0%, 100% { transform: translateY(0) rotate(0deg); }
  50% { transform: translateY(-20px) rotate(180deg); }
}

.section-title {
  text-align: center;
  margin-bottom: 3rem;
  font-size: 2.5rem;
}

.features {
  padding: 4rem 0;
}

.features-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}

.feature-card {
  text-align: center;
  padding: 2rem;
}

.feature-icon {
  font-size: 3rem;
  margin-bottom: 1rem;
  display: block;
}

.feature-card h3 {
  color: var(--primary-color);
  margin-bottom: 1rem;
}

.recent-posts {
  padding: 4rem 0;
  background: rgba(139, 69, 19, 0.05);
}

.posts-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 2rem;
  margin-bottom: 3rem;
}

.post-preview {
  padding: 2rem;
}

.post-category {
  display: inline-block;
  background: var(--accent-color);
  color: var(--text-color);
  padding: 0.3rem 0.8rem;
  border-radius: 20px;
  font-size: 0.9rem;
  font-weight: 500;
  margin-bottom: 1rem;
}

.post-preview h3 {
  margin-bottom: 1rem;
  color: var(--primary-color);
}

.post-preview p {
  margin-bottom: 1.5rem;
  color: var(--text-light);
}

.post-meta {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

</style>
