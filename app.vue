<template>
  <div class="bg-primary">
    <NuxtLayout>
      <header>
        <Header />
      </header>

      <main class="min-h-screen">
        <NuxtPage />
      </main>

      <footer>
        <Footer />
      </footer>
    </NuxtLayout>
  </div>
</template>
<style>
@import "tailwindcss";
@import "assets/css/main.css";
@reference "assets/css/main.css";
</style>
