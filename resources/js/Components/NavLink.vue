<script setup>
import { computed } from 'vue';
import { Link } from '@inertiajs/vue3';

const props = defineProps({
    href: {
        type: String,
        required: true,
    },
    active: {
        type: Boolean,
    },
});

const classes = computed(() =>
    props.active
        ? 'border-b-4 border-blue-400 font-medium leading-5 text-blue-400 focus:outline-none focus:border-blue-700 transition duration-150 ease-in-out'
        : 'border-b-4 border-transparent hover:font-medium leading-5 text-gray-500 hover:text-gray-700 hover:border-blue-400 focus:outline-none focus:text-gray-700 focus:border-blue-300 transition duration-150 ease-in-out'
);
</script>

<template>
    <Link :href="href" :class="classes">
        <slot />
    </Link>
</template>
