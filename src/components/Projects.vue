<script setup>
const projects = [
  {
    number: '01',
    title: 'Интернет-магазин',
    description:
      'Интернет-магазин с каталогом товаров, фильтрацией и корзиной.',
    tags: ['JavaScript', 'HTML', 'SCSS'],
    demo: 'https://alexanderoreshkin.github.io/skillbox_js_project/',
    github: 'https://github.com/AlexanderOreshkin/skillbox_js_project.git'
  },
  {
    number: '02',
    title: 'Сайта магазина растений',
    description:
      'Адаптивный дизайн сайта магазина растений ',
    tags: ['HTML', 'SCSS'],
    demo: 'https://alexanderoreshkin.github.io/Flowers-shop_adaptive/',
    github: 'https://github.com/AlexanderOreshkin/Flowers-shop_adaptive.git'
  },
  {
    number: '03',
    title: 'Менеджер задач',
    description:
      'Приложение для создания и управления задачами с сохранением данных в LocalStorage.',
    tags: ['JavaScript', 'Vue 3', 'LocalStorage'],
    demo: 'https://your-demo-url.com',
    github: 'https://github.com/your-username/task-manager'
  }
]
</script>

<template>
  <section id="projects" class="section">
    <div class="container">
      <div class="section-title">
        <span>03</span>
        <h2>Мои проекты</h2>
      </div>

      <div class="projects">
        <article
          v-for="project in projects"
          :key="project.number"
          class="project"
        >
          <span class="project__number">
            {{ project.number }}
          </span>

          <div class="project__content">
            <div class="project__header">
              <h3>{{ project.title }}</h3>
            </div>

            <p>
              {{ project.description }}
            </p>

            <ul class="project__tags">
              <li
                v-for="tag in project.tags"
                :key="tag"
              >
                {{ tag }}
              </li>
            </ul>

            <div class="project__links">
              <a
                :href="project.demo"
                target="_blank"
                rel="noopener noreferrer"
                class="project__link project__link--primary"
              >
                Live Demo
                <span>↗</span>
              </a>

              <a
                :href="project.github"
                target="_blank"
                rel="noopener noreferrer"
                class="project__link"
              >
                GitHub
                <span>↗</span>
              </a>
            </div>
          </div>
        </article>
      </div>
    </div>
  </section>
</template>