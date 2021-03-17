<template>
<div>
    <b-button @click=peticionDatos>Consultar</b-button>

    <ol>
        <b-card-group>
        <div v-for="oferta in resultado"
        :key="oferta.id" >
        <Oferta :infoOferta= oferta >
        </Oferta>
        
        </div>
        </b-card-group>
    </ol>
</div> 

    
</template>
<script>

import Oferta from './Oferta.vue'

export default {
   name: 'Consulta',
   data: function(){
       return{
           resultado: []
       }
   },
   components: {
     Oferta
   },
   methods:{
       peticionDatos: function(){
           console.log("una peticion a la api")
           this.axios.get('http://labs.iam.cat/~a19carerecas/2DAW/M06/Backend/api.php/records/oferta').then((response) => {
            this.resultado=response.data.records;
        })
       }
   }
}
</script>