<script setup>

import vEducationItem from './vEducationItem.vue';
import {ref} from 'vue';

const education_arr = ref([
    {
        id: 1,
        link: 'https://certs.prometheus.org.ua/downloads/d1d47c77eda34249a1b882a0652f5752/Certificate.pdf',
        gain_date: '09.10.22',
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