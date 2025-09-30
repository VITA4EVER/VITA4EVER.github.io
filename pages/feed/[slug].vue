<script setup>
const slug = useRoute().params.slug
const { data: post } = await useAsyncData(`feed-${slug}`, () => {
  return queryCollection('feed').path(`/${slug}`).first()
})
</script>

<template>
  <div class="section bg-[url('assets/pictures/bg.png')]">
    <div class="drk-rect"></div>
    <div v-if="post" class="absolute w-screen min-h-screen flex flex-col justify-center items-center pt-[5%] gap-12 text-center">
      <h2 class="text-3xl text-center font-bold">{{post.title}}</h2>
      <ContentRenderer :value="post" />
      <KZButton link="/">Go Back</KZButton>
    </div>
    <div v-else class="absolute w-screen min-h-screen flex flex-col justify-center items-center pt-[5%] gap-12 text-center">
      <h1>404 - Not Found</h1>
      <KZButton link="/">Go Back</KZButton>
    </div>
  </div>
</template>