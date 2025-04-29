<template>
  <div id="app" class="min-h-screen min-w-full flex flex-col font-sans">
    <!-- Шапка -->
    <header class="bg-gradient-to-r from-gray-600 to-sky-600 text-white p-4 fixed top-0 left-0 w-full shadow-lg">
      <div class="container mx-auto flex justify-between items-center">
        <h1
          class="text-3xl font-bold tracking-wide text-transparent bg-clip-text bg-gradient-to-r from-gray-300 to-sky-400">
          Юлия Свидзинская
        </h1>

        <!-- Меню для мобильных -->
        <button @click="toggleMenu" class="lg:hidden text-white text-2xl">☰</button>

        <!-- Навигация на больших экранах -->
        <nav class="space-x-3 gap-2.5 hidden lg:flex">
          <a href="#" class="text-lg relative group">
            Главная
            <span
              class="absolute left-0 bottom-0 w-full h-0.5 bg-blue-200 scale-x-0 transition-all duration-300 group-hover:scale-x-100"></span>
          </a>
          <a href="#" class="text-lg relative group">
            Услуги
            <span
              class="absolute left-0 bottom-0 w-full h-0.5 bg-blue-200 scale-x-0 transition-all duration-300 group-hover:scale-x-100"></span>
          </a>
          <a href="#" class="text-lg relative group">
            Обо мне
            <span
              class="absolute left-0 bottom-0 w-full h-0.5 bg-blue-200 scale-x-0 transition-all duration-300 group-hover:scale-x-100"></span>
          </a>
          <a href="#" class="text-lg relative group">
            Контакты
            <span
              class="absolute left-0 bottom-0 w-full h-0.5 bg-blue-200 scale-x-0 transition-all duration-300 group-hover:scale-x-100"></span>
          </a>
        </nav>


        <!-- Выпадающее меню для мобильных -->
        <nav v-if="menuOpen"
          class="lg:hidden absolute top-16 right-0 w-2/3 bg-sky-800 text-white p-4 transition-all duration-500 ease-in-out transform">
          <a href="#" class="block py-2 hover:underline">Главная</a>
          <a href="#" class="block py-2 hover:underline">Услуги</a>
          <a href="#" class="block py-2 hover:underline">Обо мне</a>
          <a href="#" class="block py-2 hover:underline">Контакты</a>
        </nav>
      </div>
    </header>

    <!-- Контент -->
    <main class="w-screen overflow-auto bg-gray-100 px-5">
      <div class="flex justify-center w-full space-x-8">
        <!-- Левая часть секций -->
        <div class="space-y-8 w-full lg:w-1/2">
          <section class="bg-white shadow-xl p-8 rounded-3xl bg-opacity-90">
            <h2 class="text-2xl font-semibold mb-4 text-gray-800">Астрологические услуги</h2>
            <p class="text-gray-700 leading-relaxed">
              Здесь будет описание ваших услуг Lorem ipsum dolor sit amet, consectetur adipisicing
              elit. Quasi fuga asperiores similique adipisci atque reiciendis rem ea eaque tempore!
              Velit quasi molestiae voluptatibus ullam veniam explicabo sint possimus dolorem
              tenetur.. Пример текста для демонстрации контента.
            </p>
          </section>
          <section class="bg-white shadow-xl p-8 rounded-3xl bg-opacity-90">
            <h2 class="text-2xl font-semibold mb-4 text-gray-800">Как проходит консультация</h2>
            <p class="text-gray-700 leading-relaxed">
              Опишите, как проходит ваша работа с клиентом. Пример текста для демонстрации контента.
            </p>
          </section>
          <section class="bg-white shadow-xl p-8 rounded-3xl bg-opacity-90">
            <h2 class="text-2xl font-semibold mb-4 text-gray-800">Отзывы клиентов</h2>
            <p class="text-gray-700 leading-relaxed">
              Здесь можно разместить отзывы и впечатления.
            </p>
          </section>
          <section class="bg-white shadow-xl p-8 rounded-3xl bg-opacity-90">
            <h2 class="text-2xl font-semibold mb-4 text-gray-800">Часто задаваемые вопросы</h2>
            <p class="text-gray-700 leading-relaxed">Ответьте на популярные вопросы.</p>
          </section>
        </div>

        <!-- Правая часть секций -->
        <div class="space-y-8 w-full lg:w-1/2">
          <section class="bg-white shadow-xl p-8 rounded-3xl bg-opacity-90">
            <h2 class="text-2xl font-semibold mb-4 text-gray-800">Тема 5</h2>
            <p class="text-gray-700 leading-relaxed">
              Дополнительная информация для демонстрации контента.
            </p>
          </section>
          <section class="bg-white shadow-xl p-8 rounded-3xl bg-opacity-90">
            <h2 class="text-2xl font-semibold mb-4 text-gray-800">Тема 6</h2>
            <p class="text-gray-700 leading-relaxed">
              Добавьте сюда текст, описание услуги или раздел.
            </p>
          </section>
          <section class="bg-white shadow-xl p-8 rounded-3xl bg-opacity-90">
            <h2 class="text-2xl font-semibold mb-4 text-gray-800">Тема 7</h2>
            <p class="text-gray-700 leading-relaxed">
              Здесь можно рассказать о специфике работы или услугах.
            </p>
          </section>
          <section class="bg-white shadow-xl p-8 rounded-3xl bg-opacity-90">
            <h2 class="text-2xl font-semibold mb-4 text-gray-800">Тема 8</h2>
            <p class="text-gray-700 leading-relaxed">
              Поделитесь интересной информацией или предложением.
            </p>
          </section>
        </div>
      </div>
    </main>

    <!-- Футер -->
    <footer
      class="bg-gradient-to-r from-sky-600 to-gray-800 text-center py-6 text-white p-4 fixed bottom-0 left-0 w-screen shadow-lg">
      <p>© 2025 Астролог Юлия Свидзинская. Все права защищены.</p>
      <div class="flex justify-center space-x-6 mt-4 gap-4">
        <a href="https://www.instagram.com/yulyaaach/" class="text-blue-300 relative group text-2xl">
          <i class="fab fa-instagram"></i>
          <span
            class="absolute left-0 bottom-0 w-full h-0.5 bg-blue-200 scale-x-0 transition-all duration-300 group-hover:scale-x-100"></span>
        </a>
        <a href="https://t.me/Yulya_Svidzinskaya" class="text-blue-300 relative group text-2xl">
          <i class="fab fa-telegram-plane"></i>
          <span
            class="absolute left-0 bottom-0 w-full h-0.5 bg-blue-200 scale-x-0 transition-all duration-300 group-hover:scale-x-100"></span>
        </a>
        <a href="mailto:yulya_chernikova_97@icloud.com" class="text-blue-300 relative group text-2xl">
          <i class="fas fa-envelope"></i>
          <span
            class="absolute left-0 bottom-0 w-full h-0.5 bg-blue-200 scale-x-0 transition-all duration-300 group-hover:scale-x-100"></span>
        </a>
      </div>
    </footer>

  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const menuOpen = ref(false)

const toggleMenu = () => {
  menuOpen.value = !menuOpen.value
}
</script>

<style scoped>
/* Шрифты */
@import url('https://fonts.googleapis.com/css2?family=Lora:wght@700&family=Roboto:wght@400&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Tagesschrift&display=swap');

html,
body,
#app {
  height: 100%;
  width: 100%;
  margin: 0;
  padding: 0;
}

#app {
  font-family: 'Roboto', sans-serif;
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  width: 100%;
}

header h1 {
  margin-left: 1.5rem;
  font-family: 'Tagesschrift', serif;
}

main {
  padding-top: 120px;
  /* Для того, чтобы контент не перекрывал шапку */
  padding-bottom: 60px;
  /* Для футера */
  flex-grow: 1;
  overflow-y: auto;
  display: flex;
  justify-content: center;
  align-items: flex-start;
  background-color: #f7f7f7;
  /* Светлый фон для контента */
}

main .flex {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  gap: 2rem;
}

main .space-y-8>section {
  margin-bottom: 2rem;
  padding: 2rem;
  border-radius: 16px;
  background-color: #ffffff;
}

footer {
  position: relative;
  padding: 2rem;
  text-align: center;
  background: linear-gradient(90deg, rgba(14, 165, 233, 1) 0%, rgba(31, 41, 55, 1) 100%);
  font-family: 'Roboto', sans-serif;
}
</style>
