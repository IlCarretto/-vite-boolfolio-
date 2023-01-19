<script>
export default {
    name: 'AppHeader'
}
</script>

<template>
<nav class="navbar navbar-expand-lg bg-body-tertiary">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Boolfolio</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
  </div>
  <a href="http://127.0.0.1:8000/admin">ADMIN</a>
</nav>
</template>

<style lang="scss">
@use "../styles/general.scss" as *;
</style>