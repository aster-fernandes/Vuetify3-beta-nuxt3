<template>
  <div class="container">
    <v-app>
      <section>
        <div><strong>Sample Button</strong></div>
        <v-btn>Click </v-btn>
      </section>
      <section>
        <div><strong>Sample Table</strong></div>
        <SampleTable :data="dummyTableData" />
      </section>
    </v-app>
  </div>
</template>

<script setup lang="ts">
import dummyTableData from "./data/dummyData";
const data = dummyTableData;
</script>

<style>
section {
  padding: 20px;
}
</style>
