<template>
  <div class="content">
    <div class="container-fluid">
      <div class="row">
        <div class="col-12">
          <card>
            <template slot="header">
              <h4 class="card-title"><b>Salas Agendadas</b></h4>
              
            </template>
            <div class="table-responsive">
              <l-table class="table-hover table-striped"
                       :columns="table1.columns"
                       :data="table1.data">
              </l-table>
            </div>
          </card>

        </div>
      <div class="col-12">
          <button type="button" class="btn btn-primary">
            <router-link to="agendar-horario">
              Adicionar Horário
            </router-link>
            </button>
      </div>

      </div>
    </div>
  </div>
</template>
<script>
  import LTable from 'src/components/UIComponents/Table.vue'
  import Card from 'src/components/UIComponents/Cards/Card.vue'
  const tableColumns = ['Professor', 'Data', 'Inicio', 'Fim', 'Sala', 'Editar']
  const tableData = [{
    id: 1,
    professor: 'Dakota Rice',
    data: '10/11/2018',
    inicio: '08:30',
    fim: '09:20',
    sala: 'Oud-Turnhout'
  },
  {
    id: 2,
    professor: 'Minerva Hooper',
    data: '10/11/2018',
    inicio: '08:30',
    fim: '09:20',
    sala: 'Oud-Turnhout'
  },
  {
    id: 3,
    professor: 'Sage Rodriguez',
    data: '10/11/2018',
    inicio: '08:30',
    fim: '09:20',
    sala: 'Oud-Turnhout'
  },
  {
    id: 4,
    professor: 'Philip Chaney',
    data: '10/11/2018',
    inicio: '08:30',
    fim: '09:20',
    sala: 'Oud-Turnhout'
  },
  {
    id: 5,
    professor: 'Doris Greene',
    data: '10/11/2018',
    inicio: '08:30',
    fim: '09:20',
    sala: 'Oud-Turnhout'
  }]
  export default {
    components: {
      LTable,
      Card
    },
    data () {
      return {
        table1: {
          columns: [...tableColumns],
          data: [...tableData]
        }
      }
    }
  }
</script>
<style>
</style>
