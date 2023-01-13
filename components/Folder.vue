<template>
    <div class="collapse">
        <input type="checkbox" />
        <div class="collapse-title flex">
            <ChevronDownIcon class="h-6 w-6 text-white mr-4" />
            <FolderIcon class="h-6 w-6 text-blue-500 mr-4" />
            <span class="text-white font-mono">{{ folder.name }}</span>
        </div>
        <div class="collapse-content">
            <Note v-for="note in props.notes" :note="note"></Note>
        </div>
    </div>
</template>

<script lang="ts" setup>
import { FolderIcon, ChevronDownIcon } from "@heroicons/vue/24/outline";
import Note from "./Note.vue";
const props = defineProps(["folder", "notes"]);
</script>
