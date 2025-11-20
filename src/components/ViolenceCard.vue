<template>
  <div class="bg-card rounded-2xl p-6 shadow-lg card-hover">
    <div :class="`w-12 h-12 bg-${color}-100 rounded-full flex items-center justify-center mb-4`">
      <span class="text-2xl">{{ emoji }}</span>
    </div>
    <h3 :class="`text-xl font-bold mb-2 text-${color}-600`">{{ title }}</h3>
    <p class="text-secondary mb-4">{{ description }}</p>
    <a 
      :href="link" 
      :class="`inline-block bg-${color}-600 text-white px-4 py-2 rounded-full text-sm font-semibold hover:bg-${color}-700 transition-colors`"
    >
      Más Información
    </a>
  </div>
</template>

<script>
export default {
  name: 'ViolenceCard',
  props: {
    emoji: {
      type: String,
      required: true
    },
    title: {
      type: String,
      required: true
    },
    description: {
      type: String,
      required: true
    },
    color: {
      type: String,
      default: 'purple'
    },
    link: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
.bg-card {
  background-color: var(--bg-primary);
  transition: all 0.3s ease;
}

.text-secondary {
  color: var(--text-secondary);
}

.card-hover:hover {
  transform: translateY(-5px);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
}
</style>