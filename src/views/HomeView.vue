<template>
  <div class="m-0 p-0">
    <p class="w-64 mx-auto mt-0 text-white font-bold text-7xl">
      Portifolio
    </p>
  </div>
  <div>
    <div class="pt-10 flex items-left justify-left">
      <img class="w-48 h-48 rounded-xl shadow-lg border border-gray-300 object-cover" src="../imgs/profilepic.jpeg" alt="">
    </div>
    <div> 
      <p class="pt-10 text-white max-w-md mx-left text-left text-5xl font-bold">Joaquim Moreira</p>
      <p class="pt-5 text-gray-100 max-w-md mx-left text-left text-3xl ">Em teoria DEV</p>
      <p class="pt-5 text-white max-w-md mx-left text-left text-3xl font-thin ">Olá! Meu nome é Joaquim Moreira e cada dia chego mais perto de me tornar um dev.</p>
    </div>
  </div>
  <div class="pt-10 flex gap-4">
    <button @click="$router.push('/contact')" class="bg-gradient-to-r from-[#20222e] to-[#7185eb] text-white px-4 py-2 rounded hover:opacity-50">
      Entre em contato
    </button>

    <button @click="$router.push('/about')" class="bg-gradient-to-r from-[#20222e] to-[#7185eb] text-white px-4 py-2 rounded hover:opacity-50">
      Sobre mim
    </button>
  </div>

</template>


