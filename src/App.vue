<template>
  <div id="app" class="min-h-screen flex flex-col font-sans">
    <!-- Шапка -->
    <header class="bg-sky-700 text-white p-3 fixed top-0 left-0 w-full z-50">
      <div class="container mx-auto flex justify-between items-center">
        <h1 class="text-2xl font-bold">Юлия Свидзинская</h1>

        <!-- Меню для мобильных -->
        <button @click="toggleMenu" class="lg:hidden text-white">
          ☰
        </button>

        <!-- Навигация на больших экранах -->
        <nav class="space-x-4 hidden lg:flex">
          <a href="#" class="hover:underline">Главная</a>
          <a href="#" class="hover:underline">Услуги</a>
          <a href="#" class="hover:underline">Обо мне</a>
          <a href="#" class="hover:underline">Контакты</a>
        </nav>

        <!-- Выпадающее меню для мобильных (справа) -->
        <nav v-if="menuOpen"
          class="lg:hidden absolute top-16 right-0 w-2/3 bg-purple-700 text-white p-4 transition-all duration-500 ease-in-out transform">
          <a href="#" class="block py-2 hover:underline">Главная</a>
          <a href="#" class="block py-2 hover:underline">Услуги</a>
          <a href="#" class="block py-2 hover:underline">Обо мне</a>
          <a href="#" class="block py-2 hover:underline">Контакты</a>
        </nav>
      </div>
    </header>

    <!-- Контент -->
    <main class="flex-1 px-4 py-12 space-y-8">
      <div class="flex justify-center w-full">
        <!-- Левая часть секций -->
        <div class="space-y-8 w-1/2">
          <section class="bg-white shadow-lg p-8 rounded-2xl bg-opacity-80">
            <h2 class="text-xl font-semibold mb-2 text-gray-800">Астрологические услуги</h2>
            <p class="text-gray-700">Здесь будет описание ваших услуг. Пример текста для демонстрации контента.</p>
          </section>
          <section class="bg-white shadow-lg p-8 rounded-2xl bg-opacity-80">
            <h2 class="text-xl font-semibold mb-2 text-gray-800">Как проходит консультация</h2>
            <p class="text-gray-700">Опишите, как проходит ваша работа с клиентом. Пример текста для демонстрации
              контента.</p>
          </section>
          <section class="bg-white shadow-lg p-8 rounded-2xl bg-opacity-80">
            <h2 class="text-xl font-semibold mb-2 text-gray-800">Отзывы клиентов</h2>
            <p class="text-gray-700">Здесь можно разместить отзывы и впечатления.</p>
          </section>
          <section class="bg-white shadow-lg p-8 rounded-2xl bg-opacity-80">
            <h2 class="text-xl font-semibold mb-2 text-gray-800">Часто задаваемые вопросы</h2>
            <p class="text-gray-700">Ответьте на популярные вопросы.</p>
          </section>
        </div>

        <!-- Правая часть секций -->
        <div class="space-y-8 w-1/2">
          <section class="bg-white shadow-lg p-8 rounded-2xl bg-opacity-80">
            <h2 class="text-xl font-semibold mb-2 text-gray-800">Тема 5</h2>
            <p class="text-gray-700">Дополнительная информация для демонстрации контента.</p>
          </section>
          <section class="bg-white shadow-lg p-8 rounded-2xl bg-opacity-80">
            <h2 class="text-xl font-semibold mb-2 text-gray-800">Тема 6</h2>
            <p class="text-gray-700">Добавьте сюда текст, описание услуги или раздел.</p>
          </section>
          <section class="bg-white shadow-lg p-8 rounded-2xl bg-opacity-80">
            <h2 class="text-xl font-semibold mb-2 text-gray-800">Тема 7</h2>
            <p class="text-gray-700">Здесь можно рассказать о специфике работы или услугах.</p>
          </section>
          <section class="bg-white shadow-lg p-8 rounded-2xl bg-opacity-80">
            <h2 class="text-xl font-semibold mb-2 text-gray-800">Тема 8</h2>
            <p class="text-gray-700">Поделитесь интересной информацией или предложением.</p>
          </section>
        </div>
      </div>
    </main>

    <!-- Футер -->
    <footer class="bg-sky-700 text-center py-6 text-white w-full fixed bottom-0 left-0">
      <p>© 2025 Астролог. Все права защищены.</p>
      <div class="flex justify-center space-x-6 mt-4">
        <a href="#" class="text-blue-400 hover:text-blue-600">Instagram</a>
        <a href="#" class="text-blue-400 hover:text-blue-600">Telegram</a>
        <a href="#" class="text-blue-400 hover:text-blue-600">Email</a>
      </div>
    </footer>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

// Стейт для управления открытием/закрытием меню на мобильных устройствах
const menuOpen = ref(false);

const toggleMenu = () => {
  menuOpen.value = !menuOpen.value;
};
</script>

<style scoped>
/* Контейнер для всего сайта, задаём минимальную высоту */
#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  width: 100%;
}

/* Шапка растягивается на всю ширину */
header {
  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 50;
}

/* Чтобы контент не загораживался шапкой, отступаем сверху */
main {
  padding-top: 100px;
  /* Увеличиваем отступ сверху, чтобы шапка не перекрывала контент */
  flex-grow: 1;
  /* Контент растягивается на оставшуюся высоту */
  display: flex;
  justify-content: center;
  /* Выравнивание контента по центру */
  align-items: flex-start;
}

/* Контент будет выровнен по центру с двумя колонками (левая и правая) */
main .flex {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  gap: 2rem;
  /* Отступ между колонками */
}

/* Контейнер для секций с левой и правой стороны */
main .flex>div {
  width: 48%;
  /* Контент занимает 48% ширины, оставляя отступ */
  max-width: 100%;
  /* Ограничиваем максимальную ширину */
}

/* Секции */
main .space-y-8>section {
  margin-bottom: 1.5rem;
}

/* Для футера */
footer {
  width: 100%;
  /* Растягиваем футер на всю ширину */
  position: fixed;
  bottom: 0;
  left: 0;
  padding: 1.5rem;
  text-align: center;
}
</style>