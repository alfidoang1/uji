<template>
    <nav class="navbar navbar-expand-lg bg-light">
      <NuxtLink class="navbar-brand" to="#">
        <img
          src="~/assets/img/Logo.png"
          alt="Logo"
          width="65"
          height="60"
          class="d-inline-block align-text-bootom"
        />
        SMKN 4 TASIKMALAYA
      </NuxtLink>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNavDropdown"
        aria-controls="navbarNavDropdown"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNavDropdown">
        <ul class="navbar-nav">
          <li class="nav-item">
            <NuxtLink class="nav-link active" aria-current="page" to="/">Home</NuxtLink>
          </li>
          <li class="nav-item dropdown">
            <NuxtLink
              class="nav-link dropdown-toggle"
              to="#"
              role="button"
              data-bs-toggle="dropdown"
              aria-expanded="false"
            >
              Profile
            </NuxtLink>
            <ul class="dropdown-menu">
              <li><NuxtLink class="dropdown-item" to="profile/sejarah">sejarah</NuxtLink></li>
              <li><NuxtLink class="dropdown-item" to="/visi">visi & misi</NuxtLink></li>
            </ul>
          </li>
          <li class="nav-item">
            <NuxtLink class="nav-link" to="eskul">Ekstrakulikuler</NuxtLink>
          </li>
          <li class="nav-item">
            <NuxtLink class="nav-link" to="galeri">Galeri</NuxtLink>
          </li>
        </ul>
      </div>
    </nav>
</template>
<style scoped>
.collapse {
  padding-left: 50%;
}
.navbar {
  position: fixed;
  z-index: 1;
  width: 100vw;
}
</style>
