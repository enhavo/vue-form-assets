<template>
    <component v-if="form.rowComponent !== 'form-row'" :is="form.rowComponent" :form="form" />
    <div v-else v-show="form.isVisible()">
        <form-label :form="form"></form-label>
        <form-errors :form="form"></form-errors>
        <form-widget :form="form"></form-widget>
        <form-help :form="form"></form-help>
    </div>
</template>

<script setup lang="ts">
import {Form} from "@enhavo/vue-form/model/Form";

const props = defineProps<{
    form: Form
}>()
</script>
