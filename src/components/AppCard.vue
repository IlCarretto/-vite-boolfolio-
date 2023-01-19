<script>
export default {
    name: 'AppCard',
    props: {
        project: Object
    },
    data() {
        return {
            laravelUrl: "http://127.0.0.1:8000"
        }
    },

}
</script>

<template>
    <div class="card">
        <img src="" class="card-img-top" alt="">
    </div>
    <div class="card-body">
        <h5 class="card-title">{{ project.title }}</h5>
        <p class="card-text">{{ project.proj_description }}</p>
        <a href="#" class="btn btn-primary">Leggi di più</a>
    </div>
</template>

<style lang="scss">
@use "../styles/general.scss" as *;
</style>