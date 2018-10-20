<template>
  <card>
    <h4 slot="header" class="card-title"><b>Agendamento de Salas de Aula</b></h4>
    <form>
      <div class="row">
        <div class="col-md-12">
          <fg-input type="text"
                    label="Nome do Professor"
                    :disabled="true"
                    placeholder="professor"
                    v-model="prof.name">
          </fg-input>
        </div>       
        
      </div>

      <div class="row">
        <div class="col-md-6">
          <fg-input type="text"
                    label="Sala"
                    placeholder="sala"
                    v-model="prof.sala">
          </fg-input>
        </div>
        <div class="col-md-2">
          <fg-input type="date"
                    label="Dia da Aula"
                    placeholder="dia"
                    v-model="prof.dia">
          </fg-input>
        </div>
        <div class="col-md-2">
          <fg-input type="time"
                    label="Horário Inicial"
                    placeholder="h_inicial"
                    v-model="prof.inicial">
          </fg-input>
        </div>
        <div class="col-md-2">
          <fg-input type="time"
                    label="Horário Final"
                    placeholder="h_final"
                    v-model="prof.final">
          </fg-input>
        </div>
      </div>

      <div class="row">
        <div class="col-md-12">
          <div class="form-group">
            <label>Conteúdo da Aula</label>
            <textarea rows="5" class="form-control border-input"
                      placeholder="Escreva o Conteúdo da Aula"
                      v-model="prof.content">
              </textarea>
          </div>
        </div>
      </div>
      <div class="text-center">
        <button type="submit" class="btn btn-info btn-fill float-right" @click.prevent="adicionarReserva">
          Adicionar Reserva da Sala
        </button>
      </div>
      <div class="clearfix"></div>
    </form>
  </card>
</template>
<script>
  import Card from 'src/components/UIComponents/Cards/Card.vue'

  export default {
    components: {
      Card
    },
    data () {
      return {
        prof: {
          name: 'Mike Andrew',
          sala: 'Lab. Ciências',
          dia: '21/10/2018',
          inicial: '08:00',
          final: '09:00',
          content: `Aula de Ciências`
        }
      }
    },
    methods: {
      adicionarReserva () {
        alert('Your data: ' + JSON.stringify(this.prof))
      }
    }
  }

</script>
<style>

</style>
