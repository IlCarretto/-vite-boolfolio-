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
        <router-link :to="{ name: 'project-details', params: { slug: project.slug } }" class="btn btn-primary"
                        href="">Info</router-link>
    </div>
</template>

<style lang="scss">
@use "../styles/general.scss" as *;
</style>