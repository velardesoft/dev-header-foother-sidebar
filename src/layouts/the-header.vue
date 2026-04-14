<template>
  <header class="header">
    <div class="header-content">
      <h1 class="title">
        <span class="full-name">Velarde Gonzales, Néstor Velarde</span>
        <span class="brand-tag">(velardesoft)</span>
      </h1>
    </div>
  </header>
</template>

<style scoped>
.header {
  background-color: #F8FAFC; /* Fondo profesional claro [cite: 175] */
  color: #1E293B;           /* Texto pizarra oscuro para contraste [cite: 176] */
  border-bottom: 1px solid #E2E8F0; /* Línea sutil de separación [cite: 177] */
  padding: 1rem;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.header-content {
  max-width: 1200px;
  width: 100%;
  text-align: center;
}

.title {
  margin: 0;
  display: flex;
  flex-direction: column; /* Apilado en móviles por defecto [cite: 234] */
  gap: 0.25rem;
  font-size: 1.25rem;
}

.full-name {
  font-weight: 700;
  letter-spacing: -0.025em;
}

.brand-tag {
  color: #3B82F6; /* Color de acento para tu marca [cite: 150, 233] */
  font-size: 0.9rem;
  font-family: monospace;
  font-weight: 500;
}

/* --- Ajustes Responsivos --- [cite: 234] */
@media (min-width: 768px) {
  .title {
    flex-direction: row; /* En línea para pantallas medianas/grandes */
    justify-content: center;
    align-items: baseline;
    gap: 0.75rem;
    font-size: 1.5rem;
  }
}
</style>