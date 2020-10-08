<template>
  <div class="nav">
    <div class="container">
      <b-navbar toggleable="lg" type="light">
        <b-navbar-brand href="#">
          Larue Vincent
        </b-navbar-brand>
        <b-navbar-toggle target="nav-collapse" />
        <b-collapse id="nav-collapse" is-nav>
          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto">
            <b-nav-item
              href="#"
              v-scroll-to="'#projets'"
            >
              Projets
            </b-nav-item>
            <b-nav-item
              href="#"
              v-scroll-to="'#xps'"
            >
              Experiences
            </b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>
  </div>
</template>
<style>
.nav{
  background: #f0f1f6;
}
</style>
