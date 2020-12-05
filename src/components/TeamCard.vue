<template>
    <div class="card bg-dark">
      <div class="card bg-light">
        <span class="border border-secondary">
            <img class="mx-auto d-block " :src= "imagen"/>
            <div class="card-body">
               <h5 class="card-title">{{nombre}}</h5>
               <p class="card-text " >
               <p class="text-justify">    
                   {{descripcion}}
               </p>
               <p class="card-text font-italic"><small>Rol: {{rol}}</small></p>
            </div>
            </span>
        </div>   
    </div>
</template>

<script>
    export default {
        name: "TeamCard",
        props: {
            codigo: {
                type: Number,
                required: true,

            },
            nombre: {
                type: String,
                required: true,

            },
            descripcion: {
                type: String,
                required: true,

            },
            rol: {
                type: String,
                required: true,

            },
             imagen: {
                type: String,
                required: true,

            }

        }
    }

</script>

<style scoped>


</style>

 
