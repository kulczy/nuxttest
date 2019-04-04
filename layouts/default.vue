<template>
  <div>
    <div>
      <b-navbar type="dark" variant="dark">
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

    <nuxt/>
  </div>
</template>

<style>
</style>
