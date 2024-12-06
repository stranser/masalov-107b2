<template>
  <div class="layout-default">
    <header class="layout-default__header">
      <nav>
        <a href="/users">Users</a>
      </nav>
    </header>
    <div class="layout-default__content">
      <div class="container">
        <slot name="default" />
      </div>
    </div>
    <footer class="layout-default__footer">
      <p>&copy; 2024 Your Company</p>
    </footer>
  </div>
</template>

<script setup lang="ts">
</script>

<style scoped>
.layout-default {
  width: 100%;
  height: 100%;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  background-color: aliceblue;
  overflow: hidden;
}

.layout-default__header,
.layout-default__footer {
  height: 4rem; 
  display: flex;
  justify-content: space-between;
  align-items: center; 
  background-color: aquamarine;
  padding: 0 1rem; 
}

.layout-default__header nav a {
  margin: 0 0.5rem;
  text-decoration: none;
  color: #333;
}

.layout-default__content {
  display: flex;
  flex: 1;
  align-items: flex-start; 
  justify-content: center;
  padding: 1rem; 
}

.layout-default__footer {
  text-align: center;
  background-color: #e0f7fa;
}

@media (max-width: 768px) {
  .layout-default__header,
  .layout-default__footer {
    height: 3rem; 
  }

  .layout-default__content {
    padding: 0.5rem;
  }

  .layout-default__header nav a {
    font-size: 0.9rem;
  }
}
</style>
