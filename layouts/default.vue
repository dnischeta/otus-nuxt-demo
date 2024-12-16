<template>
    <div class="layout">
        <header>
            <h1>
                <NuxtLink :to="{ name: 'index' }">
                    App
                </NuxtLink>
            </h1>
            <nav>
                <ul>
                    <li><NuxtLink :to="{ name: 'post' }">Posts</NuxtLink></li>
                </ul>
            </nav>
        </header>
        <main>
            <slot />
        </main>
        <footer>
            Nuxt App, 2024
        </footer>
    </div>
</template>

<style>
header {
    display: flex;
    height: 100px;
    align-items: center;
    padding: 1rem 2rem;
    background-color: #d3cbcb;
}

main {
    padding: 1rem 2rem;
    flex-grow: 1;
}

footer {
    padding: 1rem 2rem;
    background-color: #d3cbcb;
}

.layout {
    height: 100vh;
    display: flex;
    flex-direction: column;
}
</style>