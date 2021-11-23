<template>
    <div class="col-4">
        <h4 class="pb-4 text-dark">{{title}}</h4>
        <ul class="list-unstyled" v-if="list">
        <li v-for="(item, i) in list" :key="'C' + i" class="pb-4">
            > <a href="#" class="text-dark">{{item.link}}</a>
        </li>
        </ul>
        <div v-else>
            <p>{{txt}}</p>
            <img src="@/assets/img/avada-movers-logo.png" alt="movers logo">
        </div>
    </div>
</template>

<script>
export default {
    name: 'FooterCol',
    props: {
        list: Array,
        title: String,
        txt: String,
    },
}
</script>

<style>

</style>