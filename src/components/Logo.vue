<template>
  <!-- Animated stroke rendering of initials OH, replacing original AF path animation -->
  <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg" aria-label="Site logo OH">
    <title>Oscar Hickman</title>
    <!-- Outer circle akin to cosmic boundary / particle horizon -->
    <circle class="path-circle" cx="50" cy="50" r="46" fill="none" stroke="currentColor" stroke-width="2.5" />
    <!-- O drawn as a single path using arc to enable dash animation -->
    <path class="path-o" d="M50 14 A36 36 0 1 1 49.999 14" stroke="currentColor" stroke-width="7" fill="none" stroke-linecap="round" />
    <!-- H composed of three segments in one path for continuous stroke animation -->
    <path class="path-h" d="M25 18 L25 82 M75 18 L75 82 M25 50 L75 50" stroke="currentColor" stroke-width="7" fill="none" stroke-linecap="round" stroke-linejoin="round" />
  </svg>
</template>

<style scoped>
svg {
  display: block;
}

@media (prefers-reduced-motion) {
  .path-circle,
  .path-o,
  .path-h {
    animation: none !important;
    stroke-dasharray: none !important;
  }
}

/* Shared animation base */
.path-circle,
.path-o,
.path-h {
  stroke-dashoffset: 1px;
  stroke-dasharray: 400px 0; /* large value ensures full length covered */
  animation: draw 3.5s ease forwards;
}

.path-o {
  animation-delay: 0.2s;
}
.path-h {
  animation-delay: 1.4s;
}
.path-circle {
  animation-delay: 2.4s;
  animation-duration: 4.5s;
}

@keyframes draw {
  0% {
    stroke-dasharray: 0 400px;
    opacity: 0;
  }
  10% {
    opacity: 1;
  }
  60% {
    stroke-dasharray: 400px 0;
  }
  90% {
    stroke-dasharray: 400px 0;
  }
  100% {
    stroke-dasharray: 0 400px;
  }
}

.dark .path-circle,
.dark .path-o,
.dark .path-h {
  stroke: #fdfdfd;
}
</style>
