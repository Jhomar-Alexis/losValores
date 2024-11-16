<template>
  <div class="flex gap-10 flex-col items-center py-10 height:fit-content bg-gray-200">
    <h1 class="text-black text-2xl md:text-4xl font-[900] text-center">
      Valores en la Escuela
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
      <div class="w-60 lg:w-80 mb-4 bg-teal-800 p-4 rounded-lg shadow-[0_0_12px_0] shadow-black mx-4">
        <div class="pb-4">
          <img src="~/public/images/5.jpg" alt="Tecnología"
            class="w-full object-cover border-4 border-white rounded-lg" />
        </div>
        <div class="bg-white p-2 rounded-lg">
          <p class="text-black font-[900] text-center">Responsabilidad:</p>
          <p class="text-black font-semibold text-around">
            Los alumnos deben mostrar responsabilidad presentando sus tareas
            trabajos y exposiciones escolares que se le dejen asistiendo
            temprano a clases y sin falta mostrando su compromiso con sus
            estudios. Demostrando que es importante cumplir con nuestros
            deberes.
          </p>
        </div>
      </div>
      <div class="w-60 lg:w-80 mb-4 bg-white p-4 rounded-lg shadow-[0_0_12px_0] shadow-black mx-4">
        <div class="pb-4">
          <img src="~/public/images/7.jpg" alt="Tecnología"
            class="w-full object-cover border-4 border-teal-800 rounded-lg" />
        </div>
        <div class="bg-teal-800 p-2 rounded-lg">
          <p class="text-white font-[900] text-center">Respeto:</p>
          <p class="text-white font-semibold text-around">
            Los estudiantes deben mostrar respeto al escuchar las opiniones de
            sus compañeros o maestros ya que aveces faltan a este valor diciendo
            palabras inadecuadas. Este valor es muy importante para tener una
            buena relacion con los demas evitando los malos entendidos.
          </p>
        </div>
      </div>
      <div class="w-60 lg:w-80 mb-4 bg-teal-800 p-4 rounded-lg shadow-[0_0_12px_0] shadow-black mx-4">
        <div class="pb-4">
          <img src="~/public/images/2.jpg" alt="Tecnología"
            class="w-full object-cover border-4 border-white rounded-lg" />
        </div>
        <div class="bg-white p-2 rounded-lg">
          <p class="text-black font-[900] text-center">Solidaridad:</p>
          <p class="text-black font-semibold text-around">
            Los deben ser solidarios demostrando su apoyo a algún compañero si
            esta pasando por un momento dificil o en proyectos grupales,
            compartiendo sus cosas y siendo amigables. Ya que hay que ser bueno
            con los demas para que lo sean contigo.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
const items = [
  {
    href: '/images/11.jpg',
    titulo: "Promoviendo los valores en mi escuela :",
    contenido: "Los valores en la escuela son importantes para poder relacionarnos de manera armoniosa, sana y respetuosa con nuestros compañeros, construyendo relaciones sin violencia, ni agresión, ayudando a crear personas con etica, responsables y comprometidos."
  },
  {
    href: '/images/3.jpg',
    titulo: "La importancía de los valores en mi escuela :",
    contenido: "Los valores en la escuela deben ser promovidos por los docentes estableciendo normas de convivencia promoviendo los trabajos en equipo y hablando sobre esto a los estudiantes."
  },
]

const carouselRef = ref()

</script>