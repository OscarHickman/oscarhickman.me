<template>
  <footer class="copyright text-center op50 text-xs py6">
    <slot />
  </footer>
</template>

<style>
.no-copyright ~ .copyright {
  display: none;
}
</style>
