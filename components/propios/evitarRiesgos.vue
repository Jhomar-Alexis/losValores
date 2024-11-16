<template>
  <div class="flex gap-10 flex-col items-center py-10 height:fit-content bg-gray-200">
    <h1 class="text-black text-2xl md:text-4xl font-[900] text-center">
      Valores en el contexto social (comunidad y entorno)
    </h1>
    <div class="flex items-center justify-center w-full">
      <div class="flex flex-col-reverse lg:flex-row-reverse items-center justify-center pb-4 lg:pb-0 lg:p-4 ">
        <div
          class="flex bg-teal-800 flex-col-reverse gap-6 xl:flex-row items-center pb-4 pt-4 rounded-lg shadow-[0_0_12px_0] shadow-black w-[80%] md:w-1/2 lg:w-1/2 xl:w-1/2 lg:p-8 xl:p-10 max-w-md">

          <UCarousel ref="carouselRef" v-slot="{ item }" :items="items" :ui="{ item: 'basis-full' }"
            class="overflow-hidden relative w-[80%] bg-teal-800" indicators>
            <div class="flex px-4 flex-col-reverse xl:flex-row justify-center">
              <div class="w-full xl:w-1/2 lg:ml-4 lg:order-2 max-w-md">
                <img :src="item.href" class="w-full h-full object-cover rounded-lg border-4 border-white" />
              </div>
              <div class="w-full xl:w-1/2 lg:order-1">
           
                <h2 class="text-white text-xl font-bold mb-2">
                  {{ item.titulo }}
                </h2>
     
                <p class="text-white lg:text-xl">
                  {{ item.contenido }}
                </p>
              </div>
            </div>
          </UCarousel>
        </div>
      </div>
    </div>
    <div class="flex flex-wrap justify-center">
      <div class="w-60 lg:w-80 mb-4 bg-teal-800 p-4 rounded-lg shadow-[0_0_12px_0] shadow-black mx-4">
        <div class="pb-4">
          <img src="~/public/images/12.jpg" alt="Tecnología"
            class="w-full object-cover border-4 border-white rounded-lg" />
        </div>
        <div class="bg-white p-2 rounded-lg">
          <p class="text-black font-[900] text-center">Gratitud:</p>
          <p class="text-black font-semibold text-around">
            Debemos ser agradecidos cuando nuestro pueblo o amigos (entorno) nos demuestran su apoyo
            fisico o emocional en momentos dificiles y siempre apoyarlos cuando ellos lo necesitan.
          </p>
        </div>
      </div>
      <div class="w-60 lg:w-80 mb-4 bg-white p-4 rounded-lg shadow-[0_0_12px_0] shadow-black mx-4">
        <div class="pb-4">
          <img src="~/public/images/13.jpg" alt="Tecnología"
            class="w-full object-cover border-4 border-teal-800 rounded-lg" />
        </div>
        <div class="bg-teal-800 p-2 rounded-lg">
          <p class="text-white font-[900] text-center">Honestidad:</p>
          <p class="text-white font-semibold text-around">
            Debemos hablar siempre con la verdad evitando hablar mal de las personas que nos rodean para evitar los
            conflictos y las peleas con las demas personas.
          </p>
        </div>
      </div>
      <div class="w-60 lg:w-80 mb-4 bg-teal-800 p-4 rounded-lg shadow-[0_0_12px_0] shadow-black mx-4">
        <div class="pb-4">
          <img src="~/public/images/3.jpg" alt="Tecnología"
            class="w-full object-cover border-4 border-white rounded-lg" />
        </div>
        <div class="bg-white p-2 rounded-lg">
          <p class="text-black font-[900] text-center">Bondad:</p>
          <p class="text-black font-semibold text-around">
            Debemos ser bondadosos con los que nos rodean cuando necesitan de nuestro apoyo ya sea de manera económica,
            emocional demostrando nuestro
            afecto y compartiendo si hace falta.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
const items = [
  {
    href: '/images/8.jpg',
    titulo: "Promoviendo los valores en el contexto social :",
    contenido: "La practica de valores en nuestra comunidad y entorno nos ayuda a formar buenos lazos con las personas que nos rodean generando confianza y respeto con los demás."
  },
  {
    href: '/images/9.jpg',
    titulo: "La importancía de los valores en el contexto social :",
    contenido: "Estos valores los podemos demostrar con nuestros vecinos, amigos, compañeros y demas personas que nos rodean, además tambien cuidando nuestra comunidad y teniendo respeto por la naturaleza."
  },
]

const carouselRef = ref()

</script>