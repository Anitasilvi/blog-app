<script setup>
const { data: posts } = await useAsyncData('posts', () => {
    queryContent('/blog').find();
})
</script>

<template>
    <h1 class="text-3xl my-8">Blog Post</h1>
    Lorem ipsum dolor sit, amet consectetur adipisicing elit. Neque maiores iure ex porro cumque! Similique voluptas nihil iure, dicta animi magni. 
    Repudiandae numquam aliquid ullam veritatis perferendis eveniet. Adipisci, possimus.
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Ratione beatae culpa neque illum doloribus doloremque molestiae adipisci,
    animi cumque debitis iusto consequuntur labore incidunt ipsum consectetur ipsam, illo saepe laboriosam!
    <section class="grid md:grid-cols-3 mt-8 gap-10">
        <Post :posts="posts"/>
    </section>
    
</template>