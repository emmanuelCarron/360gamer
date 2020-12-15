<template>
  <q-page
    class="row items-center justify-evenly"
    style="background-color: black"
  >
    <q-parallax src="../statics/bg-gamer.jpg" style="height: 50em !important">
      <q-card class="my-card" style="transform: scale(0.73,0.73)">
        <q-img src="../statics/games.jpg" basic>
          <div class="absolute-bottom text-h6">Pasión por los videojuegos</div>
        </q-img>

        <q-card-section class="cardSec">
          Desde sus comienzos, en el año 2000, mi sitio es conocido por su compromiso auténtico con la satisfacción del cliente.
          Este estándar de excelencia nos ha permitido crecer hasta llegar a donde estamos ahora.
          Para más información sobre nuestros productos y servicios, contáctanos.
        </q-card-section>
      </q-card>
    </q-parallax>
  </q-page>
</template>

<script lang="ts">
import { Todo, Meta } from "components/models";
import ExampleComponent from "components/CompositionComponent.vue";
import { defineComponent, ref } from "@vue/composition-api";

// export default defineComponent({
//   name: 'PageIndex',
//   components: { ExampleComponent },
//   setup() {
//     const todos = ref<Todo[]>([
//       {
//         id: 1,
//         content: 'ct1'
//       },
//       {
//         id: 2,
//         content: 'ct2'
//       },
//       {
//         id: 3,
//         content: 'ct3'
//       },
//       {
//         id: 4,
//         content: 'ct4'
//       },
//       {
//         id: 5,
//         content: 'ct5'
//       }
//     ]);
//     const meta = ref<Meta>({
//       totalCount: 1200
//     });
//     return { todos, meta };
//   }
// });
</script>

<style lang="css">

.cardSec {
  background-color: whitesmoke;
}
</style>