<template>
    <div class="users-table">
      <div class="users-table__row">
        <div class="users-table__cell">id</div>
        <div class="users-table__cell">Имя</div>
        <div class="users-table__cell">Почта</div>
        <div class="users-table__cell">Дата создания</div>
      </div>
      <div v-for="user in users" :key="user.id" class="users-table__row">
        <div class="users-table__cell">{{ user.id }}</div>
        <div class="users-table__cell">{{ user.name }}</div>
        <div class="users-table__cell">{{ user.email }}</div>
        <div class="users-table__cell">{{ user.created }}</div>
      </div>
    </div>
    </template>
    
    <script setup lang="ts">
    import { ref, computed } from 'vue'
    
    type UserType = {
      id: number
      name: string
      email: string
      created: string | Date
    }
    
    const currentDate = new Date()
    
    const createdMockDate = computed(() => {
  return `${currentDate.getDate()}.${currentDate.getMonth() + 1}.${currentDate.getFullYear()}`
})

    
    const users = ref<UserType[]>([
      {
        id: 0,
        name: 'Ann',
        email: 'alex@alex.alex',
        created: createdMockDate.value,
      },
      {
        id: 1,
        name: 'Alex',
        email: 'ann@ann.ann',
        created: createdMockDate.value,
      },
      {
        id: 2,
        name: 'Art',
        email: 'art@art.art',
        created: createdMockDate.value,
      },
      {
        id: 3,
        name: 'you',
        email: 'you@you.you',
        created: createdMockDate.value,
      }
    ])
    </script>
    
    <style scoped>
    .users-table {
  display: flex;
  flex-direction: column;
  width: 100%;
  border-collapse: collapse; 
}

.users-table__row {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  border-bottom: 1px solid #ddd; 
}

.users-table__cell {
  min-width: 120px;
  background-color: #f4f4f4;
  border: 1px solid #ccc; 
  text-align: center;
  padding: 8px;
  font-size: 14px;
}

    </style>