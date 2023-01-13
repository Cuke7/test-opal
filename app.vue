<template>
    <div class="w-1/2 h-screen bg-black p-4 rounded-r-lg">
        <div v-for="folder in folders">
            <Folder :folder="folder" :notes="notes"></Folder>
        </div>
    </div>
</template>

<script lang="ts" setup>
import { ref } from "vue";

import Folder from "./components/Folder.vue";

const notes = ref([
    {
        title: "Another note",
        folderID: 0,
    },
    {
        title: "A note",
        folderID: 1,
    },
]);

const folders = ref([
    {
        name: "Work",
        folderID: 0,
    },
    {
        name: "Perso",
        folderID: 1,
    },
]);
</script>
