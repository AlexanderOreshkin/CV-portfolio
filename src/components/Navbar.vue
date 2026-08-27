<script setup>
import { ref } from 'vue'

const menuOpen = ref(false)

const closeMenu = () => {
  menuOpen.value = false
}
</script>

<template>
  <header class="navbar">
    <div class="container navbar__inner">
      <a href="#home" class="logo" @click="closeMenu">
        AO
      </a>

      <button
        class="menu-button"
        aria-label="Open menu"
        @click="menuOpen = !menuOpen"
      >
        <span></span>
        <span></span>
      </button>

      <nav class="navbar__nav" :class="{ 'is-open': menuOpen }">
        <a href="#about" @click="closeMenu">
          <span>01.</span> Обо мне
        </a>

        <a href="#skills" @click="closeMenu">
          <span>02.</span> Навыки
        </a>

        <a href="#projects" @click="closeMenu">
          <span>03.</span> Проекты
        </a>

        <a href="#experience" @click="closeMenu">
          <span>04.</span> Опыт
        </a>

        <a href="#contact" class="nav-contact" @click="closeMenu">
          Контакты
        </a>
      </nav>
    </div>
  </header>
</template>