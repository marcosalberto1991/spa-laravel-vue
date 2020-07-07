<template>
  <card :title="$t('Producto')">
    {{ $t("you_are_logged_in") }}
  </card>
</template>

<script>
import Vue from "vue";
import axios from 'axios'

//import FetchUsers from "~/components/FetchUsers"
export default {
  layout: 'Admin_App',

  components: {
    //	FetchUsers
  },
  middleware: "auth",

  metaInfo() {
    return { title: this.$t("Producto") };
  },
  data() {
    return {
      formulario_Producto: false,
      productos_all: [],
      editar_dato: false,
      data_foraneo_proveedor_id: [],
      datas: []
    };
  },
  mounted() {
    //this.consulta();
    alert("paso");

    this.data_foraneo();
  },
  methods: { 
    data_foraneo() {
      axios.get("api/Producto/create").then(response => {
        this.productos_all = response.data;
        this.data_foraneo_proveedor_id = response.data.proveedor_id;
        alert('consulta')
      });
    } //fin de
  }
};
</script>
