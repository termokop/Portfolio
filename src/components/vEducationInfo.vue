<script setup>

import vEducationItem from './vEducationItem.vue';
import {ref} from 'vue';

const education_arr = ref([
    {
        id: 1,
        link: 'https://certs.prometheus.org.ua/downloads/d1d47c77eda34249a1b882a0652f5752/Certificate.pdf',
        title: 'Basic of Web UA Development 2022',
        gain_date: 'October 9, 2022',
        school_title: 'Prometheus',
        school_link: 'https://prometheus.org.ua'
    },
    {
        id: 2,
        link: 'https://www.sololearn.com/certificates/CC-4I0BVHKN',
        title: 'HTML',
        gain_date: 'October 11, 2023',
        school_title: 'SoloLearn',
        school_link: 'https://www.sololearn.com/'
    },
    {
        id: 3,
        link: 'https://www.sololearn.com/certificates/CC-KPGMZUQS',
        title: 'JavaScript',
        gain_date: 'October 9, 2023',
        school_title: 'SoloLearn',
        school_link: 'https://www.sololearn.com/'
    },
    {
        id: 4,
        link: 'https://www.sololearn.com/certificates/CC-8XJSN23P',
        title: 'JavaScript Intermediate',
        gain_date: 'October 13, 2023',
        school_title: 'SoloLearn',
        school_link: 'https://www.sololearn.com/'
    },
    {
        id: 5,
        link: 'https://certs.prometheus.org.ua/downloads/48fa809162f04343a629859a79523d5d/Certificate.pdf',
        title: 'Basic of Web UA Development',
        gain_date: 'July 24, 2017',
        school_title: 'Prometheus',
        school_link: 'https://prometheus.org.ua'
    }
])

</script>

<template>
    
    <vEducationItem>

    </vEducationItem>
    
    
            {{ education_arr[0].link }}
</template>