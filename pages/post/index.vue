<script setup lang="ts">
type Post = {
    id: number;
    title: string;
    body: string;
}

const { public: { apiBase } } = useRuntimeConfig()

const { data, status } = await useFetch<Post[]>(`${apiBase}/posts`, { lazy: true });
</script>

<template>
    <h2>Posts</h2>
    <div v-if="status === 'pending'">Loading...</div>
    <ul v-else>
        <li v-for="post in data">
            <NuxtLink :key="post.id" :to="{ name: 'post-id', params: { id: post.id } }">
                Post {{ post.id }}
            </NuxtLink>
        </li>
    </ul>
</template>