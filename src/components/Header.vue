<template>
   <!--header design-->
   <header class="header">
      <a href="#" class="logo">Portfolio</a>
      
      <!-- Menu Burger -->
      <i class='bx bx-menu' ref="menuIcon" @click="toggleMenu"></i>

      <!-- Navbar -->
      <nav ref="navbar" class="navbar" :class="{ active: isMenuOpen }">
        <a href="#home" class="active">Home</a>
        <a href="#about">About</a>
        <a href="#skills">My Skills</a>
        <a href="#portfolio">Portfolio</a>
        <a href="#contact">Contact</a>
      </nav>
   </header>
</template>

<script>


export default {
  name: "Header",

  data() {
    return {
      isMenuOpen: false,
      isSticky: false,
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
    handleScroll() {
      const sections = document.querySelectorAll('section');
      const navLinks = document.querySelectorAll('header nav a');

      sections.forEach(sec => {
        const top = window.scrollY;
        const offset = sec.offsetTop - 150;
        const height = sec.offsetHeight;
        const id = sec.getAttribute('id');

        if (top >= offset && top < offset + height) {
          navLinks.forEach(link => {
            link.classList.remove('active');
            const activeLink = document.querySelector(`header nav a[href*=${id}]`);
            if (activeLink) activeLink.classList.add('active');
          });
        }
      });

      this.isSticky = window.scrollY > 100;

      // Fermer le menu après le clic sur un lien
      this.isMenuOpen = false;
    },
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
  beforeUnmount() {
    window.removeEventListener("scroll", this.handleScroll);
  },
};
</script>


<style scoped>

.header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  padding: 2rem 9%;
  background: var(--bg-color);
  display: flex;
  justify-content: space-between;
  align-items: center;
  z-index: 100;
}

.header.sticky {
  border-bottom: 0.1rem solid rgba(0, 0, 0, 0.2);
}

.navbar {
  display: flex;
  gap: 2rem;
}

.navbar a {
  font-size: 1.7rem;
  color: var(--text-color);
  transition: 0.3s;
}

.navbar a:hover,
.navbar a.active {
  color: var(--main-color);
}

/* Menu Burger */
#menu-icon {
  font-size: 3.6rem;
  color: var(--text-color);
  display: none;
  cursor: pointer;
}

/* Version mobile */
@media (max-width: 768px) {
  #menu-icon {
    display: block;
  }

  .navbar {
    position: absolute;
    top: 100%;
    left: 0;
    width: 100%;
    background: var(--bg-color);
    display: none;
    flex-direction: column;
    padding: 1rem 0;
  }

  .navbar.active {
    display: flex;
  }
}
</style>


