<template>
  <!-- Основний контейнер для всієї сторінки, що встановлює тло та центрує "плашку".
       Тут немає фонового кольору, він встановлюється в глобальних стилях для body. -->
  <div class="min-h-screen flex items-center justify-center py-8 font-inter">
    <!-- Біла "плашка" - головний контейнер для бічної панелі та основного контенту.
         Має білий фон, заокруглені кути та тінь. -->
    <div class="bg-white rounded-2xl shadow-xl flex w-full max-w-6xl min-h-[calc(100vh-4rem)] overflow-hidden">
      <!-- Бічна панель -->
      <aside class="bg-stone-100 rounded-2xl m-5 w-64 p-6 flex flex-col justify-between overflow-y-auto">
        <div>
          <!-- Заголовок меню -->
          <div class="flex items-center justify-between mb-8">
            <span class="text-xl font-semibold text-gray-800">Меню</span>
            <button class="text-gray-600 hover:text-gray-900 focus:outline-none">
              <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
              </svg>
            </button>
          </div>

          <!-- Поле пошуку -->
          <div class="relative mb-8">
            <input type="text" placeholder="Пошук" class="w-full pl-10 pr-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-indigo-500">
            <svg class="w-5 h-5 text-gray-400 absolute left-3 top-1/2 transform -translate-y-1/2" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"></path>
            </svg>
          </div>

          <!-- Розділ завдань -->
          <h3 class="text-sm font-semibold text-gray-500 uppercase mb-4">Завдання</h3>
          <ul class="space-y-2 mb-8">
            <li>
              <a href="#" class="flex items-center justify-between p-2 text-gray-700 hover:bg-indigo-100 hover:text-indigo-700 rounded-lg">
                <span class="flex items-center">
                  <svg class="w-5 h-5 mr-3" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path></svg>
                  Майбутні
                </span>
                <span class="text-xs font-semibold text-gray-500">12</span>
              </a>
            </li>
            <li>
              <a href="#" class="flex items-center justify-between p-2 text-gray-700 hover:bg-indigo-100 hover:text-indigo-700 rounded-lg">
                <span class="flex items-center">
                  <svg class="w-5 h-5 mr-3" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"></path></svg>
                  Сьогодні
                </span>
                <span class="text-xs font-semibold text-gray-500">5</span>
              </a>
            </li>
            <li>
              <a href="#" class="flex items-center justify-between p-2 text-gray-700 hover:bg-indigo-100 hover:text-indigo-700 rounded-lg">
                <span class="flex items-center">
                  <svg class="w-5 h-5 mr-3" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"></path></svg>
                  Календар
                </span>
              </a>
            </li>
            <li>
              <a href="#" class="flex items-center justify-between p-2 bg-indigo-100 text-indigo-700 rounded-lg">
                <span class="flex items-center">
                  <svg class="w-5 h-5 mr-3" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 13h6m-3-3v6m-9 1V7a2 2 0 012-2h2c.512 0 1.025.162 1.454.456l3.052 2.222c.394.288.747.538 1.1.746H19a2 2 0 012 2v4a2 2 0 01-2 2h-4.478c.228.46.386.953.475 1.482.083.43.14.86.19 1.298V21l-3.248-1.572A1.993 1.993 0 0012 19.111v1.889h.542c.49.333 1.25.753 1.93.992l.006.002h.002l.004.002.004.002h.002c.084.027.168.053.252.078.08.024.16.047.24.07.08.023.16.046.24.068.077.022.155.044.233.064.078.02.155.04.232.059.076.019.153.037.23.054.077.018.154.035.231.051.076.016.152.03.228.043.076.013.152.025.228.036.076.01.152.019.228.027.075.008.15.015.225.02.075.005.15.009.225.012.075.003.149.006.223.007.074.001.148.002.222.002h.002v.002H18a2 2 0 002-2v-4a2 2 0 00-2-2h-3.542c-.228-.46-.386-.953-.475-1.482-.083-.43-.14-.86-.19-1.298V7.892c-.228-.46-.386-.953-.475-1.482-.083-.43-.14-.86-.19-1.298L9.542 4.417z"></path></svg>
                  Дошка "Sticky Wall"
                </span>
              </a>
            </li>
          </ul>

          <!-- Розділ списків -->
          <h3 class="text-sm font-semibold text-gray-500 uppercase mb-4">Списки</h3>
          <ul class="space-y-2 mb-8">
            <li>
              <a href="#" class="flex items-center justify-between p-2 text-gray-700 hover:bg-indigo-100 hover:text-indigo-700 rounded-lg">
                <span class="flex items-center">
                  Персональні
                </span>
                <span class="text-xs font-semibold text-gray-500">3</span>
              </a>
            </li>
            <li>
              <a href="#" class="flex items-center justify-between p-2 text-gray-700 hover:bg-indigo-100 hover:text-indigo-700 rounded-lg">
                <span class="flex items-center">
                  Робочі
                </span>
                <span class="text-xs font-semibold text-gray-500">3</span>
              </a>
            </li>
            <li>
              <a href="#" class="flex items-center justify-between p-2 text-gray-700 hover:bg-indigo-100 hover:text-indigo-700 rounded-lg">
                <span class="flex items-center">
                  Список 1
                </span>
                <span class="text-xs font-semibold text-gray-500">3</span>
              </a>
            </li>
            <li>
              <a href="#" class="flex items-center p-2 text-gray-700 hover:bg-indigo-100 hover:text-indigo-700 rounded-lg">
                <svg class="w-5 h-5 mr-3" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6v6m0 0v6m0-6h6m-6 0H6"></path></svg>
                Додати новий список
              </a>
            </li>
          </ul>

          <!-- Розділ тегів -->
          <h3 class="text-sm font-semibold text-gray-500 uppercase mb-4">Теги</h3>
          <div class="flex flex-wrap gap-2 mb-8">
            <span class="px-3 py-1 bg-red-100 text-red-700 text-xs font-medium rounded-full">Тег 1</span>
            <span class="px-3 py-1 bg-blue-100 text-blue-700 text-xs font-medium rounded-full">Тег 2</span>
            <button class="px-3 py-1 bg-gray-200 text-gray-700 text-xs font-medium rounded-full hover:bg-gray-300">
              <span class="flex items-center">
                <svg class="w-3 h-3 mr-1" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6v6m0 0v6m0-6h6m-6 0H6"></path></svg>
                Додати тег
              </span>
            </button>
          </div>
        </div>

        <!-- Нижні елементи меню -->
        <div>
          <ul class="space-y-2">
            <li>
              <a href="#" class="flex items-center p-2 text-gray-700 hover:bg-indigo-100 hover:text-indigo-700 rounded-lg">
                <svg class="w-5 h-5 mr-3" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.562.343 1.25.556 1.942.556z"></path><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"></path></svg>
                Налаштування
              </a>
            </li>
            <li>
              <a href="#" class="flex items-center p-2 text-gray-700 hover:bg-indigo-100 hover:text-indigo-700 rounded-lg">
                <svg class="w-5 h-5 mr-3" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 16l4-4m0 0l-4-4m4 4H7m6 4v1a3 3 0 01-3 3H6a3 3 0 01-3-3V7a3 3 0 013-3h4a3 3 0 013 3v1"></path></svg>
                Вийти
              </a>
            </li>
          </ul>
        </div>
      </aside>

      <!-- Основний контент -->
      <main class="flex-1 p-8 overflow-y-auto">
        <h1 class="text-3xl font-bold text-gray-800 mb-8">Sticky Wall</h1>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-6">
          <!-- Динамічно відображувані картки Sticky Note -->
          <div
            v-for="(note, index) in notes"
            :key="note.id"
            :class="['p-6 rounded-2xl shadow-md relative', note.color]"
          >
            <h2 class="text-xl font-semibold text-gray-800 mb-3">{{ note.title }}</h2>
            <p class="text-gray-700 whitespace-pre-wrap">{{ note.content }}</p>
            <button @click="deleteNote(index)" class="absolute top-3 right-3 text-gray-500 hover:text-red-600 focus:outline-none">
              <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
              </svg>
            </button>
          </div>

          <!-- Картка для додавання нового елемента -->
          <div class="bg-white p-6 rounded-2xl shadow-md flex flex-col items-center justify-center border-2 border-dashed border-gray-300 hover:border-indigo-500 transition duration-300 cursor-pointer"
               @click="showAddNoteModal = true">
            <button class="text-gray-400 hover:text-indigo-600 focus:outline-none">
              <svg class="w-16 h-16" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6v6m0 0v6m0-6h6m-6 0H6"></path>
              </svg>
            </button>
            <span class="mt-4 text-gray-600">Додати нову нотатку</span>
          </div>
        </div>
      </main>
    </div>

    <!-- Модальне вікно для додавання нової нотатки (розташоване поза "плашкою" для правильного позиціонування) -->
    <div v-if="showAddNoteModal" class="fixed inset-0 bg-gray-600 bg-opacity-50 flex items-center justify-center z-50">
      <div class="bg-white p-8 rounded-lg shadow-xl w-full max-w-md">
        <h2 class="text-2xl font-bold mb-6 text-gray-800">Додати нову нотатку</h2>
        <form @submit.prevent="addNote">
          <div class="mb-4">
            <label for="noteTitle" class="block text-gray-700 text-sm font-bold mb-2">Заголовок:</label>
            <input
              type="text"
              id="noteTitle"
              v-model="newNoteTitle"
              class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
              placeholder="Введіть заголовок"
              required
            />
          </div>
          <div class="mb-4">
            <label for="noteContent" class="block text-gray-700 text-sm font-bold mb-2">Зміст:</label>
            <textarea
              id="noteContent"
              v-model="newNoteContent"
              class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline h-32 resize-none"
              placeholder="Введіть зміст нотатки"
              required
            ></textarea>
          </div>
          <div class="mb-6">
            <label for="noteColor" class="block text-gray-700 text-sm font-bold mb-2">Колір:</label>
            <select
              id="noteColor"
              v-model="newNoteColor"
              class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
            >
              <option v-for="color in availableColors" :key="color.value" :value="color.value">
                {{ color.label }}
              </option>
            </select>
          </div>
          <div class="flex items-center justify-end">
            <button
              type="button"
              @click="showAddNoteModal = false"
              class="bg-gray-300 hover:bg-gray-400 text-gray-800 font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline mr-2"
            >
              Скасувати
            </button>
            <button
              type="submit"
              class="bg-indigo-600 hover:bg-indigo-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline"
            >
              Додати нотатку
            </button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, watch } from 'vue';

// Реактивні змінні для керування нотатками
const notes = ref([]);
const showAddNoteModal = ref(false);
const newNoteTitle = ref('');
const newNoteContent = ref('');
const newNoteColor = ref('bg-yellow-100'); // Колір за замовчуванням

// Доступні кольори для нотаток
const availableColors = [
  { label: 'Жовтий', value: 'bg-yellow-100' },
  { label: 'Синій', value: 'bg-blue-100' },
  { label: 'Рожевий', value: 'bg-pink-100' },
  { label: 'Помаранчевий', value: 'bg-orange-100' },
  { label: 'Зелений', value: 'bg-green-100' },
  { label: 'Фіолетовий', value: 'bg-purple-100' },
];

// Завантаження нотаток з localStorage при ініціалізації
const savedNotes = localStorage.getItem('stickyNotes');
if (savedNotes) {
  notes.value = JSON.parse(savedNotes);
} else {
  // Початкові статичні дані, якщо localStorage порожній
  notes.value = [
    {
      id: 1,
      title: 'Соціальні медіа',
      content: 'Плануйте соціальний контент\nСтворюйте календар контенту\nПлануйте просування та розповсюдження',
      color: 'bg-yellow-100',
    },
    {
      id: 2,
      title: 'Контент-стратегія',
      content: 'Потрібен час для збору інформації (цілі, персони, бюджет, аудит), але після цього було б добре зібрати мою команду (почати з SEO-фахівця), а потім, можливо, маркетолога електронної пошти. Також потрібно провести мозковий штурм щодо інструментарію.',
      color: 'bg-blue-100',
    },
    {
      id: 3,
      title: 'A/B-тести електронної пошти',
      content: 'Теми листів\nВідправник\nCTA\nЧас відправлення',
      color: 'bg-pink-100',
    },
    {
      id: 4,
      title: 'Банерна реклама',
      content: 'Примітки з воркшопу:\nПитання розміру\nЗначення має зовнішній вигляд\nЦільова сторінка повинна відповідати рекламі',
      color: 'bg-orange-100',
    },
  ];
}


// Збереження нотаток у localStorage при кожній зміні
watch(notes, (newVal) => {
  localStorage.setItem('stickyNotes', JSON.stringify(newVal));
}, { deep: true });

// Функція для додавання нової нотатки
function addNote() {
  if (newNoteTitle.value.trim() && newNoteContent.value.trim()) {
    notes.value.push({
      id: Date.now(), // Унікальний ID
      title: newNoteTitle.value,
      content: newNoteContent.value,
      color: newNoteColor.value,
    });
    // Очистити поля та закрити модальне вікно
    newNoteTitle.value = '';
    newNoteContent.value = '';
    newNoteColor.value = 'bg-yellow-100'; // Скинути колір за замовчуванням
    showAddNoteModal.value = false;
  }
}

// Функція для видалення нотатки
function deleteNote(index) {
  notes.value.splice(index, 1);
}
</script>

<style>
/* Глобальні стилі, включно з шрифтом Inter та скролбаром */
body {
  margin: 0;
  font-family: 'Inter', sans-serif;
  /* Встановлюємо оливковий фон для всієї сторінки, як на зображенні */
  background-color: #d4dbca !important; /* Приблизний оливковий відтінок */
}

/* Кастомні стилі для скролбару (опціонально) */
::-webkit-scrollbar {
    width: 8px;
}
::-webkit-scrollbar-track {
    background: #f1f1f1;
    border-radius: 10px;
}
::-webkit-scrollbar-thumb {
    background: #888;
    border-radius: 10px;
}
::-webkit-scrollbar-thumb:hover {
    background: #555;
}
</style>
