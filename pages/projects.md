---
title: Projects - Oscar Hickman
display: Projects
description: Projects
wrapperClass: 'text-center'
art: dots
---

<script setup>
const projects = {
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
