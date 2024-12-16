<template>
    <h2>Posts</h2>
    <ul>
        <li><NuxtLink :to="{ name: 'post-id', params: { id: 1 } }">Post 1</NuxtLink></li>
        <li><NuxtLink :to="{ name: 'post-id', params: { id: 2 } }">Post 2</NuxtLink></li>
        <li><NuxtLink :to="{ name: 'post-id', params: { id: 3 } }">Post 2</NuxtLink></li>
    </ul>
</template>