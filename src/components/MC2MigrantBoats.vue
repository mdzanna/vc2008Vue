<template>
  <b-container>
    <b-row>
      <b-col> <!-- inizio la struttura della pagina-->
        <b-form-group label="Select a year"> <!-- copiato dalla documentazione -->
          <b-form-checkbox-group
            v-model="year.value"
            :options="year.options"
            name="buttonsYear"
            buttons
          ></b-form-checkbox-group> <!-- il valore di questa riga e di quella sotto dipendono dai valori che ho bisogno di usare -->
        </b-form-group>  <!-- i valori li creo sotto nella funzione data(), <script> -->
      </b-col>
      <b-col>
        <b-form-group label="Select a boat type"> <!-- uguale a quello sopra -->
          <b-form-checkbox-group
            v-model="boatType.value"
            :options="boatType.options"
            name="buttonsBoats"
            buttons
          ></b-form-checkbox-group>
        </b-form-group>
      </b-col>
    </b-row>
    <b-row class="map">
      <b-col cols="9">
        <h3>Map</h3>
        <div style="height:400px; background-color: beige"></div>
      </b-col>
      <b-col>
        <h3>Counters</h3>
        <div style="height:400px; background-color: beige"></div>
      </b-col>
    </b-row>
    <b-row class="plots">
      <b-col>
        <h5>Year</h5>
        <div style="height:200px; background-color: beige"></div>
      </b-col>
      <b-col>
        <h5>Boat Type</h5>
        <div style="height:200px; background-color: beige"></div>
      </b-col>
      <b-col>
        <h5>Interdictions</h5>
        <div style="height:200px; background-color: beige"></div>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  name: 'MC2MigrantBoats',
  data() {
    return {
      year: {
        value: 2001,
        options: [2001, 2002, 2003],
      },
      boatType: {
        value: 'All',
        options: ['All','Rustic','Raft'],
      },
    };
  },
};
</script>

<style scoped>

</style>
