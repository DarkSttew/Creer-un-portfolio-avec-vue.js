<script setup>
    import TitreNiveau2 from './TitreNiveau2.vue';

    const parcours = {
        annee1: {
            ecole: 'Collège Jean Castel',
            date: 'De 2012 à 2016',
            title: 'Diplôme National du Brevet',
            comment: 'Mention Assez Bien .'
        },
        annee2: {
            ecole: 'Lycée Jules Verne',
            date: 'De 2017 à 2020',
            title: 'Baccalauréat STI2D - Système Numérique',
            comment: 'Mention Assez Bien - Spécialité Informatique et Numérique.'
        },
        annee3: {
            ecole: 'Centre européen de formation',
            date : 'De 2024 à 2026',
            title: 'Titre Professionnel Développeur Web et Web Mobile (DWWM)',
            comment: 'Technologies : HTML - CSS - JavaScript - Vue.Js - Git/GitHub '
        },
    }
</script>

<template>
    <div class="courses">
        <div class="courses__title">
            <span class="material-symbols-outlined">school</span><br>
            <TitreNiveau2>Mon parcours</TitreNiveau2>
        </div>
    
        <div class="parcours">
            <div class="ecole" v-for="annee in parcours">
                <h3 class="ecole__title">{{ annee.ecole }}</h3>
                <h4 class="ecole__info">{{ annee.title }} <span class="separation">|</span> {{ annee.date }}</h4>
                <p class="ecole__comment">{{ annee.comment }}</p>
            </div>
        </div>
    </div>
</template>

<style scoped>
    .courses {
        width: 60%;
        display: flex;
        flex-direction: column;
        align-items: center;
        margin: auto;
    }

    .courses__title {
        text-align: center;
    }

    .material-symbols-outlined {
        font-size: 4em;
    }

    .ecole__title {
        font-size: 1.25em;
    }

    .ecole__info {
        font-size: 1.05em;
    }

    .separation {
        font-style: italic;
        color: #A0006D;
    }

    .ecole__comment {
        text-indent: 2em;
        text-align: justify;
    }

    .parcours {
        margin-top: 15px;
        display: flex;
        flex-direction: column-reverse;
        gap: 25px;
    }

    .ecole {
        padding: 15px;
        background-color: #EFFAFD;
        border-radius: 25px;
        box-shadow: -4px 5px 10px #060640;
    }

    @media screen and (max-width: 480px) {
        .courses {
            width: 85%;
        }
    }
</style>