<template>

  <section class="section bg-[url('assets/pictures/bg.png')]">
    <div class="drk-rect"></div>
    <div class="absolute w-screen min-h-screen flex flex-col justify-center items-center pt-[5%] gap-12 text-center">
      <img class="w-full md:w-[80%] lg:w-[40%]" src="/assets/pictures/logo.png" >
      <h2 class="font-bold text-4xl">We are VITA4EVER</h2>
      <p>Hey there! We revive old games! Why? Because we want to preserve their legacy!</p>
      <p>We revived <b>Killzone Mercenary</b> on PlayStation Vita! We call it Mirage.</p>
      <p>Bellow are the buttons for tutorials:</p>

      <KZButton link="https://youtu.be/8oDXjPDfyYQ">Mirage Tutorial Video</KZButton>
      <KZButton link="https://mirage.yuv.pink/guide/">Mirage Text Tutorial</KZButton>

      <p>You can interact with our community on our Discord server here:</p>
      <KZButton link="https://discord.gg/9mCpDAUmUn" >Join Discord</KZButton>
    </div>
  </section>

</template>
<style>
@import "tailwindcss";
@import "assets/css/main.css";
@reference "assets/css/main.css";

</style>

<script>
export default {
  methods: {
    do_alert(alert_message) {
      alert(alert_message);
    }
  }
}
</script>