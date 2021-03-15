<template>
  <div>
      <h2>Resultado: {{varA}} {{operacion}} {{varB}} = {{igual}}</h2>
      <div class="pantalla">
          <pre>
            {
                "a": {{varA}},
                "b": {{varB}},
                "c": {{igual}},
                "operador": "{{operacion}}" 
            }  
          </pre>
      </div>
  </div>
</template>

<script>
export default {
    props:
    ['varA','varB','operacion', 'igual'],
    name: 'Resultado',
}
</script>

<style>
    .pantalla{
        width: 100%;
        height: auto;
        background-color: aquamarine;
    }
</style>