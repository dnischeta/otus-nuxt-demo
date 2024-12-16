<script setup lang="ts">
type Post = {
    id: number;
    title: string;
    body: string;
}

const route = useRoute()
const { public: { apiBase } } = useRuntimeConfig()


const { data, status } = await useFetch<Post>(
    `${apiBase}/posts/${route.params.id}`,
    { lazy: true, watch: [computed(() => route.params.id)] },
);
</script>

<template>
    <h1 v-if="status === 'pending'">Loading...</h1>
    <template v-else>
        <h1 >Post {{ data!.title }}</h1>
        <p>{{ data!.body }}</p>
    </template>
</template>