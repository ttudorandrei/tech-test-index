<template>
  <div class="h-full">
    <Header />

    <!-- main content -->
    <main class="absolute top-20 grid grid-cols-1 w-screen">
      <Hero />

      <Content />
    </main>
    <Footer />
  </div>
</template>

<script>
export default {
  name: "main-page",
};
</script>
