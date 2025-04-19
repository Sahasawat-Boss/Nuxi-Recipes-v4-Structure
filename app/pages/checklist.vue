<template>
    <section class="max-w-screen-lg mx-auto px-6 py-12">
        <h2 class="text-3xl font-semibold mb-4">Checklist</h2>
        <p class="text-lg mb-6">
            Keep track of everything you need to get done.
        </p>

        <!-- Add new task -->
        <div class="flex gap-2 mb-6">
            <input
                v-model="newTask"
                @keyup.enter="addTask"
                type="text"
                placeholder="Add a new task..."
                class="flex-1 border border-gray-400 px-4 py-2 rounded-md focus:outline-none focus:ring-2 focus:ring-amber-500"
            />
            <button
                @click="addTask"
                class="bg-amber-600 text-white px-4 py-2 rounded-md hover:bg-amber-700"
            >
                Add
            </button>
        </div>

        <!-- Todo List -->
        <ul class="grid grid-cols-1 md:grid-cols-2 gap-2 text-lg">
            <li
                v-for="(todo, index) in todos"
                :key="index"
                class="flex justify-between items-center bg-white/70 rounded-md px-4 py-2 shadow-sm"
            >
                <label class="flex gap-2 items-center w-full">
                    <input
                        class="hidden peer"
                        type="checkbox"
                        v-model="todo.completed"
                    />
                    <div
                        class="relative w-6 h-6 rounded-full border-2 border-dodgeroll-gold flex items-center justify-center peer-checked:after:absolute peer-checked:after:w-4 peer-checked:after:h-4 peer-checked:after:bg-amber-500 peer-checked:after:rounded-full"
                    ></div>
                    <span class="peer-checked:line-through break-words flex-1">
                        {{ todo.task }}
                    </span>
                </label>

                <!-- Delete button -->
                <button
                    @click="deleteTask(index)"
                    class="text-red-500 hover:text-red-700 text-sm ml-4"
                    title="Delete"
                >
                    ✕
                </button>
            </li>
        </ul>
    </section>
</template>

<script setup lang="ts">
import { ref } from "vue";

useSeoMeta({
    title: "Nuxi Recipes | Checklist",
});

const todos = ref([
    { task: "Buy fresh ingredients", completed: false },
    { task: "Prep the kitchen", completed: false },
    { task: "Using Nuxi Recipes App", completed: true },
]);

const newTask = ref("");

const addTask = () => {
    const taskText = newTask.value.trim();
    if (taskText) {
        todos.value.push({ task: taskText, completed: false });
        newTask.value = "";
    }
};

const deleteTask = (index: number) => {
    todos.value.splice(index, 1);
};
</script>
