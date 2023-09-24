<script setup>
const { data: posts } = await useAsyncData('posts', () =>
  queryContent('/blog').find()
)
</script>

<template>
  <h1 class="text-3xl my-8">Blog Posts</h1>

  Lorem ipsum dolor, sit amet consectetur adipisicing elit. Perferendis illum reiciendis voluptatem dicta doloribus pariatur facere, architecto obcaecati fugiat, itaque harum a. Temporibus quas accusantium esse nobis velit unde eaque!
  Lorem ipsum dolor sit, amet consectetur adipisicing elit. Sed deleniti quae est. Corrupti iste sed pariatur molestiae dolor, quibusdam qui ab eum, eaque minus obcaecati sequi cum est nam dolorem.

  <section class="grid md:grid-cols-3 mt-8 gap-10">
    <Post :posts="posts" />
  </section>
</template>