<script setup>
// props - onMounted, reactive, ref
import { onMounted, reactive, ref } from 'vue';
import ListPersonagens from '../components/ListPersonagens.vue';


let personagens = reactive(ref())

//fetch - axios
onMounted(() => {
  fetch("https://rickandmortyapi.com/api/character")
  .then(response => response.json())
  .then(response => {
    personagens.value = response.results
    console.log(personagens)
  });
})

</script>

<template>
  <main>
    <div class="container">
      <div class="row sm-12">
        <!-- <div class="col-sm-12 col-md-6">
          <div class="card" style="width: 18rem">
            <div class="card-body">
              <h5 class="card-title">Personagem</h5>
              <p class="card-text">Série Ricky and Morty</p>
            </div>
          </div> 
        </div> -->
        <div class="">
          <div class="card md-6">
            <div class="card-body row">
              <h4 class="card-title">Personagens</h4>
              <p class="card-text">Série: <b>Ricky and Morty</b></p>
              <ListPersonagens
              v-for="personagem in personagens"
              :name="personagem.name"
              :status="personagem.status"
              :species="personagem.species"
              :gender="personagem.gender"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>