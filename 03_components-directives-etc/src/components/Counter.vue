<template>
    <section id="counter" class="flex flex-col items-center justify-center  min-h-[60vh] bg-gray-100 px-4">
        <div class="heading text-center mb-8">
            <h1 v-html="counterHeading"
                class="text-4xl md:text-5xl  audioWide font-semibold text-gray-800 font-audioWide">
            </h1>
            <Dots />
        </div>

        <div class="counter-app flex flex-col items-center bg-white p-8 rounded-xl shadow-lg w-full max-w-xs">
            <span class="status mt-2 text-sm mb-4 audioWide text-blue-400 font-medium">
                {{ count % 2 != 0 ? "Odd Number" : "Even Number" }}
            </span>
            <span v-bind:class="textColor" class="text-5xl font-bold mb-6">{{ count }}</span>


            <div class="btns flex gap-6">

                <button @click="decrement" :disabled="dcButtonDisabled"
                    :class="[pointer, dcButtonDisabled ? 'opacity-50 cursor-not-allowed' : '', 'bg-red-600 text-white px-6 py-2 rounded-md hover:bg-red-500 transition-all duration-200']">
                    Decrement
                </button>

                <button v-on:click="increment"
                    :class="[pointer, 'bg-blue-600 text-white px-6 py-2 rounded-md hover:bg-blue-500 transition-all duration-200']">
                    Increment
                </button>


            </div>
        </div>

    </section>
</template>

<script>
import Dots from './Dots.vue';


export default {
    components: {
        Dots
    },
    data() {
        return {
            pointer: "cursor-pointer",
            textColor: "text-gray-600",
            disabledStyling: "",
            counterHeading: "<h1>Counter App</h1>",
            dcButtonDisabled: false,
            count: 0
        }
    },
    methods: {

        increment() {
            this.count++;
            this.dcButtonDisabled = false;
            this.textColor = this.count > 10 ? "text-green-500" : "text-gray-600";
        },

        decrement() {
            if (this.count > 0) {
                this.count--;
            }

            if (this.count <= 0) {
                this.count = 0;
                this.dcButtonDisabled = true;
            }

            this.textColor = this.count > 10 ? "text-green-500" : "text-gray-500";
        }

    }
};

</script>

<style scoped></style>


<!-- 
    DIRECTIVES  
    v-html: Is a directvie in Vue.js and it use to return raw html
-->