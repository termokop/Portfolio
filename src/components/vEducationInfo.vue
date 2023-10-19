<script setup>

import vEducationItem from './vEducationItem.vue';
import {ref} from 'vue';

const openLink = link => {
    window.open(link)
}

const education_arr = ref([
{
        id: 0,
        link: 'src/assets/Diplomas/PNPU.png',
        img_path: 'src/assets/Diplomas/PNPU_sm.jpg',
        title: 'Teacher of physics',
        gain_date: 'June 30, 2018',
        school_title: 'PNPU',
        school_link: 'https://pnpu.edu.ua/'
    },
    {
        id: 1,
        link: 'https://certs.prometheus.org.ua/downloads/d1d47c77eda34249a1b882a0652f5752/Certificate.pdf',
        img_path: 'src/assets/certificates/WebUI2022_Promet.png',
        title: 'Basic of Web UA Development 2022',
        gain_date: 'October 9, 2022',
        school_title: 'Prometheus',
        school_link: 'https://prometheus.org.ua'
    },
    {
        id: 2,
        link: 'https://www.sololearn.com/certificates/CC-4I0BVHKN',
        img_path: 'src/assets/certificates/html_SL.png',
        title: 'HTML',
        gain_date: 'October 11, 2023',
        school_title: 'SoloLearn',
        school_link: 'https://www.sololearn.com/'
    },
    {
        id: 3,
        link: 'https://www.sololearn.com/certificates/CC-KPGMZUQS',
        img_path: 'src/assets/certificates/JS_SL.png',
        title: 'JavaScript',
        gain_date: 'October 9, 2023',
        school_title: 'SoloLearn',
        school_link: 'https://www.sololearn.com/'
    },
    {
        id: 4,
        link: 'https://www.sololearn.com/certificates/CC-8XJSN23P',
        img_path: 'src/assets/certificates/JSInterm_SL.png',
        title: 'JavaScript Intermediate',
        gain_date: 'October 13, 2023',
        school_title: 'SoloLearn',
        school_link: 'https://www.sololearn.com/'
    },
    {
        id: 5,
        link: 'https://certs.prometheus.org.ua/downloads/48fa809162f04343a629859a79523d5d/Certificate.pdf',
        img_path: 'src/assets/certificates/WebUI_Promet.png',
        title: 'Basic of Web UA Development',
        gain_date: 'July 24, 2017',
        school_title: 'Prometheus',
        school_link: 'https://prometheus.org.ua'
    },
    {
        id: 6,
        link: 'https://www.sololearn.com/certificates/CC-FDNRLWMO',
        img_path: 'src/assets/certificates/GameDevWJS_SL.png',
        title: 'Game Development with JS',
        gain_date: 'October 17, 2023',
        school_title: 'SoloLearn',
        school_link: 'https://www.sololearn.com/'
    }
])

</script>

<template>
    <div class="education-info">
        <vEducationItem v-for="certificate of education_arr" :key="certificate.id">
            <template #title>
                {{certificate.title}}
            </template>
            <template #screen-shot>
                <img class="certificate-img" :src="certificate.img_path" :alt="certificate.title" @click="openLink(certificate.link)"/>
            </template>
        </vEducationItem>
    </div>
    
</template>

<style scope>

    .certificate-img {
        width: 100%;
        border: black 1px solid;
    }
    .education-info {
        margin: 0;
        padding: 0;
        width: 100%;
        display: flex;
        flex-wrap: wrap;
        cursor: pointer;
    }

</style>