<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue'

const isBottom = ref(false)

const handleScroll = () => {
  const totalPageHeight = document.documentElement.scrollHeight
  const scrollPosition = window.innerHeight + window.scrollY
  
  if (totalPageHeight - scrollPosition <= 60) {
    isBottom.value = true
  } else {
    isBottom.value = false
  }
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll, { passive: true })
  handleScroll()
})

onBeforeUnmount(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<template>
  <a 
    href="https://media.danielkaufman.dev" 
    target="_blank" 
    class="dkd-floating-badge" 
    :class="{ 'is-expanded': isBottom }"
    aria-label="Built by DKD Media"
  >
    <span class="badge-dot"></span>
    <span class="badge-text-wrapper">
      <span class="badge-text">Built by <strong>DKD Media</strong></span>
    </span>
  </a>
</template>

<style scoped>
.dkd-floating-badge {
  --brand-primary: #e65c00;
  --brand-secondary: #e65c00a5;

  position: fixed;
  bottom: 20px;
  right: 20px;
  z-index: 9999;
  display: flex;
  align-items: center;
  justify-content: flex-start;
  background-color: #13161a;
  border: 1px solid rgba(255, 255, 255, 0.08);
  height: 30px;
  padding: 0 11px;
  border-radius: 20px;
  text-decoration: none;
  box-shadow: 0 0 8px rgba(0, 0, 0, 0.5);
  max-width: 30px; 
  overflow: hidden;
  transition: max-width 0.4s cubic-bezier(0.25, 1, 0.5, 1), 
              border-color 0.2s ease, 
              padding 0.4s cubic-bezier(0.25, 1, 0.5, 1);
}

.badge-dot {
  width: 8px;
  height: 8px;
  background-color: var(--brand-primary);
  border-radius: 50%;
  flex-shrink: 0;
  box-shadow: 0 0 6px var(--brand-secondary);
  animation: pulse-glow 2s infinite ease-in-out;
}

.badge-text-wrapper {
  max-width: 0;
  opacity: 0;
  white-space: nowrap;
  display: inline-flex;
  align-items: center;
  height: 100%;
  transition: max-width 0.4s cubic-bezier(0.25, 1, 0.5, 1), 
              opacity 0.25s ease, 
              margin-left 0.4s ease;
}

.badge-text {
  color: #8a929b;
  font-family: 'Inter', sans-serif;
  font-size: 0.75rem;
  letter-spacing: 0.5px;
  padding-right: 4px;
  display: inline-flex;
  align-items: center;
  line-height: 1;
}

.badge-text strong {
  color: #ffffff;
  font-weight: 600;
  margin-left: 4px;
}

.dkd-floating-badge:hover,
.dkd-floating-badge.is-expanded {
  max-width: 220px;
  padding: 0 16px;
  border-color: var(--brand-primary);
}

.dkd-floating-badge:hover .badge-text-wrapper,
.dkd-floating-badge.is-expanded .badge-text-wrapper {
  max-width: 180px;
  opacity: 1;
  margin-left: 10px;
}

@keyframes pulse-glow {
  0%, 100% {
    transform: scale(1);
    box-shadow: 0 0 6px var(--brand-secondary);
  }
  50% {
    transform: scale(1.15);
    box-shadow: 0 0 14px var(--brand-primary);
  }
}

@media (max-width: 768px) {
  .dkd-floating-badge {
    bottom: 16px;
    right: 16px;
  }
}
</style>