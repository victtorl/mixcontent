<template>
    <div class="flex flex-col mb-8 md:mb-auto gap-3.5 flex-1 p-4 mt-16">
    <h2 class="flex gap-3 items-center m-auto text-lg font-bold md:flex-col md:gap-2">
        <svg stroke="currentColor" fill="none" stroke-width="1.5" viewBox="0 0 24 24" stroke-linecap="round"
            stroke-linejoin="round" class="h-6 w-6" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg">
            <path d="M10.29 3.86L1.82 18a2 2 0 0 0 1.71 3h16.94a2 2 0 0 0 1.71-3L13.71 3.86a2 2 0 0 0-3.42 0z"></path>
            <line x1="12" y1="9" x2="12" y2="13"></line>
            <line x1="12" y1="17" x2="12.01" y2="17"></line>
        </svg>Lista de entradas
    </h2>
    <ul class="flex flex-col gap-3.5 w-full sm:max-w-md m-auto" v-for="item in itemsblog" >
        <NuxtLink :to="`blogs/${item.slug}`" >
            <li class="w-full bg-gray-100 p-3 rounded-md cursor-pointer">{{ item.title }}</li>
        </NuxtLink>
       
    </ul>
</div>
</template>


<script setup>

const itemsblog=ref([
    {
        title:'Como usar el resultado de un promesa',
        id:0,
        slug:'resultado-de-una-promesa'
    },
    {
        title:'Como usar el operador ternario',
        id:1,
        slug:'usar-operador-ternario'

    },
    {
        title:'Crear un proyecto con NUXT',
        id:2,
        slug:'crear-proyecto-con-nuxt'
    },
    {
        title:'Crear un proyecto con NUXT',
        id:3,
        slug:'crear-proyecto-con-nuxt'
    },
])

</script>