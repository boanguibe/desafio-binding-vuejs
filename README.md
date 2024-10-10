# Vue 3 + Vite

# Desafío - Binding de formularios (I)

Este proyecto es parte de un desafío evaluado del bootcamp en Vue.js, en el cual se validan los conocimientos del **data binding** a través de directivas en Vue.js. La aplicación permite el llenado dinámico de los datos de una tarjeta de crédito, reflejados en tiempo real en la vista.

## Descripción

El objetivo de este desafío es crear una aplicación en Vue.js que incluya un formulario para llenar dinámicamente los datos de una tarjeta de crédito. El formulario y el diseño de la tarjeta ya están disponibles en el material de apoyo del desafío, por lo que tu tarea principal será implementar el código Vue.js necesario y realizar las modificaciones requeridas.

## Requerimientos

1. **Enlace bidireccional (v-model)**: Enlazar el valor de los inputs con el estado de manera bidireccional.
2. **Interpolación**: Interpolar en las etiquetas correspondientes las variables del estado. 
3. **Estado de la tarjeta**: Crear las variables del estado que almacenen la información de la tarjeta. 
4. **Binding unidireccional**: Enlazar las rutas de las imágenes utilizando binding unidireccional en el atributo `src`. 

## Código de Ejemplo

```html
<template>
    <form>
        <!-- Inputs del formulario -->
        <div>
            <label>Título de la tarjeta: </label>
            <input v-model="nombreTarjeta" />
        </div>

        <!-- Más inputs aquí -->
    </form>

    <!-- Vista dinámica de la tarjeta -->
    <div class="carnet">
        <h3> {{ nombreTarjeta }}</h3>
        <img width="40" :src="chipSrc" alt="" />
        <!-- Más contenido dinámico aquí -->
    </div>
</template>

<script>
export default {
    data() {
        return {
            nombreTarjeta: "",
            chipSrc: "",
            numeroTarjeta: "",
            fechaExpiracion: "",
            propietario: "",
            tipoTarjetaSrc: ""    
        }
    }
}
</script>
```
## Pasos para correr el proyecto

1. Descarga la aplicación.
2. Abre el proyecto en Visual Studio Code.
3. Abre un terminal y ejecuta el comando npm install para instalar las dependencias y los módulos necesarios.
4. Ejecuta npm run dev para iniciar el servidor de desarrollo.
5. ¡Listo! Ahora puedes probar la aplicación y ver el llenado dinámico de la tarjeta.

## Creditos
Aplicación desarrollada por Boris Guiñez como parte de un desafío del módulo de Vue.js en su bootcamp.

