<template>
  <footer class="footer">
    <div class="footer-container">
      <p class="copyright">
        <span class="year">© 2024</span>
        <span class="brand">Velarde-cody software</span>
      </p>

      <nav class="footer-nav">
        <a href="#" class="footer-link">Términos</a>
        <a href="#" class="footer-link">Privacidad</a>
      </nav>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  background-color: #F8FAFC; /* Fondo profesional claro [cite: 145] */
  color: #64748B;           /* Texto secundario legible [cite: 152] */
  border-top: 1px solid #E2E8F0; /* Separación sutil [cite: 154, 215] */
  padding: 1.5rem 1rem;
  width: 100%;
}

.footer-container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  flex-direction: column; /* Apilado en móviles */
  align-items: center;
  gap: 1rem;
}

.copyright {
  margin: 0;
  font-size: 0.9rem;
  display: flex;
  gap: 0.5rem;
}

.brand {
  font-weight: 600;
  color: #1E293B; /* Resalte para tu marca [cite: 148] */
}

.footer-nav {
  display: flex;
  gap: 1.5rem;
}

.footer-link {
  color: #94A3B8;
  text-decoration: none;
  font-size: 0.85rem;
  transition: color 0.2s ease;
}

.footer-link:hover {
  color: #3B82F6; /* Acento en hover [cite: 150] */
}

/* --- Ajustes Responsivos --- */
@media (min-width: 768px) {
  .footer-container {
    flex-direction: row; /* En línea para escritorio */
    justify-content: space-between;
  }
}
</style>