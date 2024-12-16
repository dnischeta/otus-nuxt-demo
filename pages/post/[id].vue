<script setup lang="ts">
const route = useRoute()
const postContent = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed vehicula est eget felis rhoncus convallis. Nullam sed quam dui. Pellentesque varius turpis at nisl luctus, eu blandit velit euismod. Sed at libero lorem. Sed tristique dolor non nisl varius, at congue tellus rutrum. Vivamus non auctor est. Maecenas pulvinar dignissim risus et laoreet. Curabitur velit justo, gravida id sapien ac, condimentum tincidunt risus. Duis sit amet elit et justo congue varius a sed neque. Nunc non convallis tortor. Fusce in efficitur augue. Pellentesque ut eros enim. Quisque consectetur lacus vel felis condimentum malesuada.'
</script>

<template>
    <h1>Post {{ route.params.id }}</h1>
    <p>{{ postContent }}</p>
</template>