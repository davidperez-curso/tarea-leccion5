<template>
  
    <div>
        <div class="input-group">
            <input type="number" class="form-control" v-model="varA" >
            <select class="custom-select" id="inputGroupSelect04" aria-label="Example select with button addon" v-model="operacion" >
                <option selected>Elige...</option>
                <option value="+">+</option>
                <option value="-">-</option>
                <option value="*">*</option>
                <option value="/">/</option>
            </select>
            <input type="number" class="form-control" v-model="varB" >
            <div class="input-group-append">
                <button class="btn btn-outline-danger" type="button" @click="calcular">Calcular</button>
            </div>
        </div>
        <Resultado class="my-4" :varA="varA" :varB="varB" :operacion="operacion" :igual="igual" /> 

    </div>
</template>

<script>

import Resultado from './Resultado'

export default {
    name: 'Home',
    components: {
        Resultado
        },
    data (){
    return{
        varA: "",
        varB: "",
        operacion: "",
        igual:""
    }
    },
    methods:{
        calcular(){
            this.igual = (eval(this.varA + this.operacion + this.varB))
        }
    }
}
</script>
