<script setup>
import TheHeader from "@/layouts/the-header.vue";
import TheFooter from "@/layouts/the-footer.vue";
import TheSidebar from "@/layouts/the-sidebar.vue";
import TutorialManagement from "@/contexts/learning/pages/tutorial-management.page.vue";
</script>

<template>
  <div class="layout">
    <TheHeader />
    <div class="main-content">
      <the-sidebar />
      <main class="content">
        <TutorialManagement />
      </main>
    </div>
    <TheFooter />
  </div>
</template>

<style scoped>
.layout {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
.main-content {
  width: 100%;
  display: flex;
  flex: 1;
}
.content {
  flex: 1;
  padding: 20px;
}
</style>