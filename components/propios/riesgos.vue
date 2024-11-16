<template>

  <div class="flex gap-10 flex-col items-center py-10 height:fit-content bg-teal-800">
    <h1 class="text-white text-2xl md:text-4xl font-[900] text-center">
      Valores en la Familia
    </h1>

    <div class="flex items-center justify-center w-full">
      <div class="flex flex-col-reverse lg:flex-row-reverse items-center justify-center pb-4 lg:pb-0 lg:p-4 ">
        <div
          class="flex items-center justify-center bg-teal-800 flex-col-reverse gap-6 xl:flex-row pb-4 pt-4 rounded-lg shadow-[0_0_12px_0] shadow-black w-[90%] md:w-1/2 lg:w-1/2 xl:w-1/2 lg:p-8 xl:p-10">

          <UCarousel ref="carouselRef" v-slot="{ item }" :items="items" :ui="{ item: 'basis-full' }"
            class="overflow-hidden relative w-full bg-teal-800" indicators>
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
      <div class="w-60 lg:w-80 mb-4 bg-white p-4 rounded-lg shadow-[0_0_12px_0] shadow-black mx-4">
        <div class="pb-4">
          <img src="~/public/images/3.jpg" alt="Tecnología"
            class="w-full object-cover border-4 border-teal-800 rounded-lg" />
        </div>
        <div class="bg-teal-800 p-2 rounded-lg">
          <p class="text-white font-[900] text-center">Generosidad:</p>
          <p class="text-white font-semibold text-around">
            Debemos de ser compartidos con lo que tenemos estar disponibles cuando alguien de la familia se sienta
            triste para ofrecer
            apoyo, compartir nuestro tiempo sin pedir nada a cambio.
          </p>
        </div>
      </div>
      <div class="w-60 lg:w-80 mb-4 bg-teal-800 p-4 rounded-lg shadow-[0_0_12px_0] shadow-black mx-4">
        <div class="pb-4">
          <img src="~/public/images/6.jpg" alt="Tecnología"
            class="w-full object-cover border-4 border-white rounded-lg" />
        </div>
        <div class="bg-white p-2 rounded-lg">
          <p class="text-black font-[900] text-center">Amor:</p>
          <p class="text-black font-semibold text-around">
            El valor fundamental de una familia debe ser el amor y demostrar cuánto aprecian al otro demostrando su
            afecto con
            muestras como un abrazo, una palabra de apoyo, entre otras. Respetando, cuidando y apoyando en todo
            momento.
          </p>
        </div>
      </div>
      <div class="w-60 lg:w-80 mb-4 bg-white p-4 rounded-lg shadow-[0_0_12px_0] shadow-black mx-4">
        <div class="pb-4">
          <img src="~/public/images/5.jpg" alt="Tecnología"
            class="w-full object-cover border-4 border-teal-800 rounded-lg" />
        </div>
        <div class="bg-teal-800 p-2 rounded-lg">
          <p class="text-white font-[900] text-center">Empatía:</p>
          <p class="text-white font-semibold text-around">
            Como familia debemos ser empáticos escuchando a los demás miembros sin juzgarlos y sin reprochar sus
            sentimientos
            cuando necesitan ser escuchados. Celebrar sus triunfos y derrotas y apoyar sus decisiones.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
const items = [
  {
    href: '/images/6.jpg',
    titulo: "Promoviendo los valores en mi familia :",
    contenido: "Los valores en nuestra familia son fundamentales para poder tener una relación saludable con los demás integrantes y para vivir de manera armoniosa teniendo comunicación."
  },
  {
    href: '/images/10.jpg',
    titulo: "La importancía de los valores en mi familia :",
    contenido: "Los padres pueden servir de ejemplo para sus hijos utilizando los valores en sus acciones diarias, realizando actividades en familia donde se promuevan estos valores y enseñando en las tareas y responsabilidades del hogar lo importante que son los valores."
  },
]

const carouselRef = ref()

</script>