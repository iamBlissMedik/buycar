<template>
  <!-- home hero -->
  <div
    class="relative h-screen w-full bg-no-repeat bg-bottom bg-cover bg-[url('https://mysterio.yahoo.com/mysterio/api/8964DB5E909CACD18049306AFDB356D51F83B94D69A71CF8364374A44354E9D0/autoblog/resizefill_w1062_h597;quality_80;format_webp;cc_31536000;/https://s.aolcdn.com/os/ab/_cms/2021/10/12164830/2022-Lexus-LX-600-Ultra-Luxury-action-desert-front.jpg')]"
  >
    <!--home hero text -->

    <div class="z-10 absolute w-full h-full flex justify-center items-center">
      <div class="text-center font-serif w-1/2">
        <h1 class="text-8xl mb-10 text-white">Find Your Car</h1>
        <!-- search bar -->
        <CarSearchBar />
      </div>
    </div>
    <!-- dark background -->
    <div class="z-1 absolute w-full h-full bg-black opacity-50"></div>
  </div>
</template>
