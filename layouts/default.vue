<template>
  <div
    class="relative flex min-h-screen flex-col justify-center overflow-hidden bg-gray-50 py-6 md:py-12"
  >
    <div
      class="absolute inset-0 bg-[url(/img/grid.svg)] bg-center [mask-image:linear-gradient(180deg,white,rgba(255,255,255,0))]"
    />
    <div
      class="relative bg-white px-5 py-8 shadow-xl ring-1 ring-gray-900/5 md:mx-auto md:max-w-3xl md:rounded-lg md:px-10"
    >
      <slot />
    </div>
  </div>
</template>
