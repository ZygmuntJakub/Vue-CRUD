<script lang="ts" setup>
defineProps(["options", "defaultOptionText"]);
</script>

<template>
    <div class="inline-block relative w-full">
        <select
            class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 bg-white leading-tight focus:outline-none focus:shadow-outline"
        >
            <option disabled value="">{{ defaultOptionText }}</option>
            <option
                v-for="option in options"
                :key="option.id"
                :value="option.id"
                class="text-gray-700"
            >
                {{ option.text }}
            </option>
        </select>
        <div
            class="pointer-events-none absolute inset-y-0 right-0 flex items-center px-2 text-gray-700"
        >
            <svg
                class="fill-current h-4 w-4"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 20 20"
            >
                <path
                    d="M9.293 12.95l.707.707L15.657 8l-1.414-1.414L10 10.828 5.757 6.586 4.343 8z"
                />
            </svg>
        </div>
    </div>
</template>
