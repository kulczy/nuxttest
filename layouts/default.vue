<template>
  <div>
    <div>
      <b-navbar type="light" variant="white">
        <b-navbar-nav>
          <li class="nav-item">
            <nuxt-link to="/" class="nav-link">Home page</nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link to="/about" class="nav-link">About</nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link to="/contact" class="nav-link">Contact</nuxt-link>
          </li>
        </b-navbar-nav>
      </b-navbar>
    </div>
    <div class="container mt-4">
      <div class="row">
        <nuxt/>
      </div>
    </div>
  </div>
</template>

<style>
</style>
