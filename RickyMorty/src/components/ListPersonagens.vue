<script setup>
    const personagem = defineProps(["name", "status", "species","gender", "url"])
    // const idPersonagem = personagem.url.split('/')[6]
</script>

<template>
    <div class="col-md-4">
        <div class="card mb-3">
            <div class="card-body">
                <p class="card-title">{{ personagem.name }}</p>
                <p class="card-text">{{ personagem.status }}</p>
                <p class="card-text">{{ personagem.species }}</p>
                <p class="card-text">{{ personagem.gender }}</p>
            </div>
        </div>
    </div>
</template>
