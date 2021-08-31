<template>
  <div class="container-fluid py-4 table-child">
    <table class="table">
      <thead class="thead-light">
        <tr>
          <th>BE Nummer</th>
          <th>BE Typ</th>
          <th>Konzerneigentümer</th>
          <th>Nutzer</th>
          <th>Besitzfläche</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for='item in tableData' :key='item'>
          <td scope="row">{{ item.nummer }}</td>
          <td>{{ item.typ }}</td>
          <td>{{ item.konzern }}</td>
          <td>{{ item.nutzer }}</td>
          <td>{{ item.besitzfläche }}</td>
        </tr>
      </tbody>
    </table>
  </div>


</template>
<script>

export default {
 name: 'Table',
  data(){
    return{
      tableData : [
        { 
          nummer: 'AD0000001742',
          typ : 'Besitz BE',
          konzern : 'DB Netz AG (BK16)',
          nutzer : 'Netz Projekte',
          besitzfläche : '3.036'
        },
        { 
          nummer: 'AD0000001942',
          typ : 'Besitz BE1',
          konzern : 'DB Netz AG (BK16)',
          nutzer : 'Netz Projekte',
          besitzfläche : '3.038'
        },
        { 
          nummer: 'AD0000001942',
          typ : 'Besitz BE2',
          konzern : 'DB Netz AG (BK16)',
          nutzer : 'Netz Projekte',
          besitzfläche : '3.037'
        },
      ]
      
    } 
  } 
}

</script>
<style scoped>
.table-child {
  overflow-y: auto;
  height: 25rem;
}

label {
  font-size: 0.8em;
  color: #222222;
}

th {
  font-size: 0.8em !important;
  color: #222222;
  font-weight: 300;
}

td {
  font-size: 0.8em;
}
</style>
