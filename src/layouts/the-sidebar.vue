<script setup>
import { ref } from 'vue';

const activeRoute = ref('home');

const navigationItems = [
  { id: 'home', label: 'Home', icon: '🏠' },
  { id: 'about', label: 'About', icon: '👤' },
  { id: 'contact', label: 'Contact', icon: '✉️' }
];

const setActive = (id) => {
  activeRoute.value = id;
};
</script>

<template>
  <aside class="sidebar">
    <nav class="sidebar-nav">
      <ul class="nav-list">
        <li v-for="item in navigationItems" :key="item.id">
          <a
              href="#"
              class="nav-link"
              :class="{ active: activeRoute === item.id }"
              @click.prevent="setActive(item.id)"
          >
            <span class="icon">{{ item.icon }}</span>
            <span class="link-text">{{ item.label }}</span>
          </a>
        </li>
      </ul>
    </nav>
  </aside>
</template>

<style scoped>
/* Contenedor principal con altura dinámica profesional [cite: 256, 258] */
.sidebar {
  background-color: #F1F5F9;
  border-right: 1px solid #E2E8F0;
  min-height: 100dvh;
  width: 260px;
  transition: width 0.3s ease;
}

.sidebar-nav {
  padding: 1.5rem 1rem;
}

.nav-list {
  list-style: none;
  padding: 0;
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

/* Estilo base del enlace [cite: 193] */
.nav-link {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 0.75rem 1rem;
  text-decoration: none;
  color: #64748B;
  border-radius: 8px;
  font-weight: 500;
  transition: all 0.2s ease;
}

/* Transición de sombreado y color reactiva [cite: 194, 272] */
.nav-link:hover,
.nav-link.active {
  background-color: #DBEAFE; /* Fondo de destaque suave */
  color: #3B82F6;           /* Color de acento profesional [cite: 150] */
}

/* Responsividad mejorada [cite: 248] */
@media (max-width: 768px) {
  .sidebar { width: 80px; }
  .link-text { display: none; }
  .nav-link { justify-content: center; }
}

@media (max-width: 480px) {
  .sidebar {
    position: fixed;
    bottom: 0;
    width: 100%;
    min-height: auto;
    border-top: 1px solid #E2E8F0;
    z-index: 100;
  }
  .nav-list { flex-direction: row; justify-content: space-around; }
}
</style>