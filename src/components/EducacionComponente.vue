<script setup>
import { ref } from 'vue';

const timelineData = ref([
  { title: 'Escuela secundaria completa', date: '2018-2023', description: 'Rio Atuel 4-202' },
  { title: 'Tecnicatura en programacion', date: 'En proceso', description: 'UTN San Rafael' },
]);
</script>


<template>
  <div class="educacion">
    <div class="timeline">
      <div 
        v-for="(item, index) in timelineData" :key="index" class="timeline-item"
      >
        <div class="timeline-content">
          <h3 class="timeline-title">{{ item.title }}</h3>
          <span class="timeline-date">{{ item.date }}</span>
          <p>{{ item.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>


<style scoped>
.educacion {
  text-align: center;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  color: var(--vt-c-white-mute);
  margin-top: 2rem;
}

.timeline {
  position: relative;
  margin: 0 auto;
  padding: 2rem;
  width: 80%;
}

.timeline-item {
  margin: 1rem 0;
  padding-left: 1.5rem;
  position: relative;
}

.timeline-content {
  background: var(--vt-c-indigo);
  padding: 1rem;
  border-radius: 8px;
  box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
}

.timeline-title {
  margin: 0;
  font-size: 1.2rem;
  color: var(--vt-c-white);
}

.timeline-date {
  display: block;
  font-size: 0.9rem;
  color: rgb(209, 183, 148);
}
</style>
