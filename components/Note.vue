<template>
    <div class="flex mb-3 hover:bg-opacity-40 cursor-pointer bg-white bg-opacity-0 p-2 rounded-md">
        <DocumentTextIcon class="h-6 w-6 text-pink-400 mr-4" />
        <span>
            {{ props.note.title }}
        </span>
    </div>
</template>

<script lang="ts" setup>
import { DocumentTextIcon } from "@heroicons/vue/24/outline";
const props = defineProps(["note"]);
</script>
