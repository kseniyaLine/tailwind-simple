<template>
  <div>
    <header class="bg-blue-500 py-4">
      <div class="container mx-auto">
        <h1 class="text-white text-3xl font-semibold">Мой Проект</h1>
      </div>
    </header>
    <div class="container mx-auto mt-8">
      <h2 class="text-2xl font-semibold mb-4">Привет, мир!</h2>
      <div class="grid grid-cols-3 gap-4">
        <div
          v-for="card in cards"
          :key="card.id"
          class="bg-white p-4 rounded shadow"
        >
          <h3 class="text-lg font-semibold">{{ card.title }}</h3>
          <p>{{ card.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        { id: 1, title: "Карточка 1", description: "Описание первой карточки" },
        { id: 2, title: "Карточка 2", description: "Описание второй карточки" },
        {
          id: 3,
          title: "Карточка 3",
          description: "Описание третьей карточки",
        },
      ],
    };
  },
};
</script>

<style scoped>
.container {
  padding: 0 20px;
}
.card {
  background-color: #fff;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}
</style>
