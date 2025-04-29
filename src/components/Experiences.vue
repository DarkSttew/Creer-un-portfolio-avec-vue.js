<script setup>
    import TitreNiveau2 from './TitreNiveau2.vue';

    const parcours = {
        annee1: {
            entreprise: 'Stefano Toselli',
            date: 'Septembre 2021-Mai 2022',
            title: 'Ouvrier agro-alimentaire',
            comment: "Missions :Préparation des sauces bolognaise et des différentes preparations de lasagnes ; Mise en barquette des lasagnes et des sauces ; Étiquetage des barquettes ; Mise en carton des barquettes."
        },
        annee2: {
            entreprise: 'Mcdonald s',
            date: 'Juillet 2022-Septembre 2025',
            title: 'Équipier polyvalent - CDI étudiant',
            comment: "Missions : Encaissement des clients ; Préparation des commandes ; Réception des marchandises ; Gestion de la propreté de l'établissement."
        },
        annee3: {
            entreprise: 'Carrefour City',
            date: 'Septembre 2023-Décembre 2023',
            title: 'Employé libre service - CDD 3 mois',
            comment: "Missions : Encaissement des clients ; Mise en rayon des produits ;Comptage des caisses ; Gestion des stocks ; Réception des marchandises."
        },
    }
</script>

<template>
    <div class="experience">
        <div class="experience__title">
            <span class="material-symbols-outlined">work</span><br>
            <TitreNiveau2>Mes expériences professionnelles</TitreNiveau2>
        </div>
    
        <div class="annee">
            <div class="job" v-for="annee in parcours">
                <h3 class="job__title">{{ annee.entreprise }}</h3>
                <h4 class="job__info">{{ annee.title }} <span class="separation">|</span> {{ annee.date }}</h4>
                <p class="job__comment">{{ annee.comment }}</p>
            </div>
        </div>
    </div>
</template>

<style scoped>
    .experience {
        width: 60%;
        display: flex;
        flex-direction: column;
        align-items: center;
        margin: auto;
    }

    .experience__title {
        text-align: center;
    }

    .material-symbols-outlined {
        font-size: 4em;
    }

    .job__title {
        font-size: 1.25em;
    }

    .job__info {
        font-size: 1.05em;
    }

    .separation {
        font-style: italic;
        color: #A0006D;
    }

    .job__comment {
        text-indent: 2em;
        text-align: justify;
    }

    .annee {
        margin-top: 15px;
        display: flex;
        flex-direction: column-reverse;
        gap: 25px;
    }

    .job {
        padding: 15px;
        background-color: #EFFAFD;
        border-radius: 25px;
        box-shadow: -4px 5px 10px #060640;
    }

    @media screen and (max-width: 480px) {
        .experience {
            width: 85%;
        }
    }
</style>