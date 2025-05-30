<script setup lang="ts">
import Dots from './Dots.vue';

</script>

<template>
    <section id="todo" class="flex flex-col items-center justify-start min-h-[60vh] bg-gray-100 px-4 py-10">
        <h1 class="text-4xl md:text-5xl audioWide font-semibold text-gray-800 font-audioWide">Todo App</h1>
        <Dots />
        <div
            class="w-full max-w-5xl flex flex-col md:flex-row items-start md:items-center justify-between my-6 gap-6 bg-white p-6 rounded-lg shadow-lg">
            <!-- Input Area -->
            <div class="flex-1 w-full">
                <div class="flex flex-col sm:flex-row items-stretch gap-4">
                    <input type="text" placeholder="Add your tasks here..."
                        class="flex-1 px-4 py-3 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-orange-400 text-gray-700" />
                    <button
                        class="bg-orange-500 text-white px-6 py-3 rounded-md hover:bg-orange-600 transition-all duration-200">
                        Add Task
                    </button>
                </div>
            </div>

            <!-- Tasks Display Area -->
            <div class="flex-1 w-full">
                <div class="tasks bg-gray-50 border border-dashed border-orange-300 p-4 rounded-md min-h-[100px]">
                    <!-- Tasks will appear here -->
                </div>
            </div>
        </div>
    </section>
</template>

<script>

</script>
