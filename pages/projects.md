---
title: Projects - Oscar Hickman
display: Projects
description: Projects that I created or maintaining.
wrapperClass: 'text-center'
art: dots
---

<script setup>
const projects = {
  'Academic Projects': [
    {
      name: 'CMB Cosmology with Advanced Sampling',
      link: 'https://github.com/OscarHickman/cosmology-from-the-cmb-with-advanced-sampling-techniques',
      desc: 'Hamiltonian Monte Carlo and NUTS sampling for CMB cosmological parameter inference using TensorFlow Probability',
      icon: 'i-carbon-wave-direction'
    },
    {
      name: 'Photon BEC Phase Characterisation',
      link: 'https://github.com/OscarHickman/characterisation-of-photon-bec-phase-diagram-using-machine-learning',
      desc: 'Machine learning methods for characterizing photon Bose-Einstein condensate phase diagrams',
      icon: 'i-carbon-machine-learning-model'
    },
    {
      name: 'GALFORM Analysis',
      link: 'https://github.com/OscarHickman/galform_analysis',
      desc: 'Python library for analyzing GALFORM galaxy formation simulations with mass function computation and convergence testing',
      icon: 'i-carbon-chart-scatter'
    }
  ],
  'Assembly Projects': [
    {
      name: 'Connect 4 GLCD',
      link: 'https://github.com/OscarHickman/connect4_glcd',
      desc: 'A Connect 4 game implementation for graphical LCD displays',
      icon: 'i-carbon-chip'
    }
  ]
}
</script>

<ListProjects :projects="projects" />
