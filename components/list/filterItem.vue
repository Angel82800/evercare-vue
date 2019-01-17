<template>
    <v-layout class="layout" column>
        <h4>{{ title }}</h4>
        <v-select
          :items="items"
          label=""
        ></v-select>
        <span class="example">Example: {{ example }}</span>
        <span v-if="learn_more_title">Learn More About <a :href="learn_more_url">{{ learn_more_title }}</a></span>
    </v-layout>
</template>
<style lang="scss" scoped>
span {
    font-size: 10px;
}
span.example {
    margin-top: -10px;
}

.layout {
    padding: 10px;
}
</style>

<script>
export default {
    props: ['title', 'items', 'label', 'example', 'learn_more_title', 'learn_more_url']
}
</script>
