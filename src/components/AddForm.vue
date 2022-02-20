<script setup lang="ts">
import { reactive, ref } from "@vue/reactivity";
import Input from "@/components/commons/Input.vue";
import Select from "@/components/commons/Select.vue";
import Textarea from "@/components/commons/Textarea.vue";
import Button from "@/components/commons/Button.vue";
import Header from "@/components/commons/Header.vue";
import Description from "@/components/commons/Description.vue";

const companies = ref([
    { id: 1, text: "The Coca-Cola Company" },
    { id: 2, text: "PepsiCo." },
    { id: 3, text: "Keurig Dr Pepper" },
]);
const state = reactive({ companies });
</script>

<template>
    <div class="flex justify-center align-middle h-full p-4">
        <div class="flex flex-col justify-center items-center w-1/4">
            <Header>Add form</Header>
            <Description>Please provide details for your ad</Description>
            <Input class="my-5" placeholder="Name" type="text" />
            <Input class="my-5" placeholder="Price" type="number" />
            <Select
                class="my-5"
                :options="state.companies"
                defaultOptionText="Please select company"
            />
            <Textarea class="my-5" placeholder="description" />
            <Button class="bg-slate-100">Submit</Button>
        </div>
    </div>
</template>
