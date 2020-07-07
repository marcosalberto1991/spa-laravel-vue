<template>
  <div class="main-layout">
    <navbaradmin/>

    <div class="container mt-4">
      <child />
    </div>
  </div>
</template>

<script>
import navbaradmin from '~/components/NavbarAdmin'


export default {
  name: 'Admin_AppLayout',
   components: {
    navbaradmin
  }
}
</script>

<style lang="scss">
.basic-layout_a {
  color: #ee1010;
  height: 100vh;
  font-weight: 100;
  position: relative;

  .links > a {
    color: #ee1010;
    padding: 0 25px;
    font-size: 12px;
    font-weight: 600;
    letter-spacing: .1rem;
    text-decoration: none;
    text-transform: uppercase;
  }
}
</style>
