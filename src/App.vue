<template>
  <div id="app">
    <!-- Header with circular profile picture -->
    <header class="header">
      <div class="container">
        <h1>Francis Frederick L. Encomienda</h1>
        <p class="subtitle">BSCS-SS231 Student</p>
        
        <!-- Circular Profile Picture -->
        <div class="profile-container">
          <img 
            src="/images/profile/20210620_103703.jpg" 
            alt="Francis Encomienda" 
            class="profile-pic"
          />
        </div>
      </div>
    </header>

    <!-- Navigation -->
    <nav class="nav">
      <div class="container">
        <a href="#about" @click="scrollToSection('about')">About</a>
        <a href="#skills" @click="scrollToSection('skills')">Skills</a>
        <a href="#projects" @click="scrollToSection('projects')">Projects</a>
        <a href="#digital-art" @click="scrollToSection('digital-art')">Digital Art</a>
        <a href="#games" @click="scrollToSection('games')">Games</a>
        <a href="#contact" @click="scrollToSection('contact')">Contact</a>
      </div>
    </nav>

    <!-- Main Content -->
    <main class="main">
      <!-- About Section -->
      <section id="about" class="section">
        <div class="container">
          <h2>About Me</h2>
          <div class="about-content">
            <p>Hello! I'm Francis Frederick L. Encomienda, a BSCS-SS231 student passionate about technology, digital art, and gaming. I enjoy creating digital artwork and working on programming projects.</p>
          </div>
        </div>
      </section>

      <!-- Skills Section -->
      <section id="skills" class="section">
        <div class="container">
          <h2>Skills</h2>
          <div class="skills-grid">
            <div class="skill-card">Digital Art</div>
            <div class="skill-card">Photo Editing</div>
            <div class="skill-card">Web Development</div>
            <div class="skill-card">Graphic Design</div>
          </div>
        </div>
      </section>

      <!-- Projects Section -->
      <section id="projects" class="section">
        <div class="container">
          <h2>Projects</h2>
          <div class="project-card">
            <h3>AGHAMamazingQuest CMS</h3>
            <p>An APC-DOST Project - A content management system for educational purposes.</p>
          </div>
        </div>
      </section>

      <!-- Digital Art Section -->
      <section id="digital-art" class="section">
        <div class="container">
          <h2>Digital Art</h2>
          <div class="art-gallery">
            <div class="art-item" v-for="(art, index) in artImages" :key="index">
              <img :src="art.path" :alt="art.alt" />
            </div>
          </div>
        </div>
      </section>

      <!-- Games Section -->
      <section id="games" class="section">
        <div class="container">
          <h2>Favorite Games</h2>
          <div class="games-grid">
            <div class="game-card" v-for="(game, index) in gameImages" :key="index">
              <img :src="game.path" :alt="game.alt" />
            </div>
          </div>
        </div>
      </section>

      <!-- Contact Section -->
      <section id="contact" class="section">
        <div class="container">
          <h2>Contact</h2>
          <div class="contact-info">
            <p>Email: <a href="#" class="placeholder-link">Coming Soon</a></p>
            <p>GitHub: <a href="https://github.com/apcflencomienda" target="_blank" class="link">github.com/apcflencomienda</a></p>
          </div>
        </div>
      </section>
    </main>

    <!-- Footer -->
    <footer class="footer">
      <div class="container">
        <p>&copy; 2025 Francis Encomienda. All rights reserved.</p>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      artImages: [
        { path: '/images/art/ARTPRE1.jpg', alt: 'Digital Art 1' },
        { path: '/images/art/Bladerunner2049 mosaic from Cedric Encomienda.jpg', alt: 'Digital Art 2' },
        { path: '/images/art/wallpaperflare.com_wallpaper.png', alt: 'Digital Art 3' }
      ],
      gameImages: [
        { path: '/images/games/bf1 logo.png', alt: 'Battlefield 1' },
        { path: '/images/games/city skyline logo.png', alt: 'Cities Skylines' },
        { path: '/images/games/project reality.png', alt: 'Project Reality' },
        { path: '/images/games/war thunder logo.png', alt: 'War Thunder' },
        { path: '/images/games/zzz logo.png', alt: 'ZZZ Game' }
      ]
    }
  },
  methods: {
    scrollToSection(sectionId) {
      const element = document.getElementById(sectionId)
      if (element) {
        element.scrollIntoView({ behavior: 'smooth' })
      }
    }
  }
}
</script>