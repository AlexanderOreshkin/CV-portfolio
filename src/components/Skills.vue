<script setup>
const groups = [
  {
    title: 'Frontend',
    skills: [
      'HTML5',
      'CSS3',
      'SCSS / Sass',
      'JavaScript',
      'Vue 3',
      'Адаптивная вёрстка'
    ]
  },
  {
    title: 'Инструменты',
    skills: [
      'Git',
      'GitHub',
      'Vite',
      'npm',
      'Figma'
    ]
  },
  {
    title: 'Изучаю',
    skills: [
      'TypeScript',
      'REST API',
      'Vue Router',
      'Pinia'
    ]
  }
]
</script>

<template>
  <section id="skills" class="section skills-section">
    <div class="container">
      <div class="section-title">
        <span>02</span>
        <h2>Навыки</h2>
      </div>

      <div class="skills">
        <article
          v-for="group in groups"
          :key="group.title"
          class="skill-card"
        >
          <p class="skill-card__title">
            {{ group.title }}
          </p>

          <ul>
            <li v-for="skill in group.skills" :key="skill">
              <span>✦</span>
              {{ skill }}
            </li>
          </ul>
        </article>
      </div>
    </div>
  </section>
</template>