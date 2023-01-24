<script>
import axios from 'axios';
export default {
    name: "ProjectDetails",
    data() {
        return {
            laravelUrl: "http://127.0.0.1:8000",
            project: {}
        }
    },
    created() {
        const slug = this.$route.params.slug;
        axios.get(`${this.laravelUrl}/api/projects/${slug}`).then(resp => {
            if (resp.data.success) {
                // Caso del post trovato
                this.project = resp.data.project;
            } else {
                // post non trovato => reindirizzo nella pagina not found
                this.$router.push({ name: "not-found" });
            }
        });
    }
}
</script>

<template>
    <main>
        <div class="container">
            <h1 class="mt-3 text-center">{{ project.title }}</h1>
            <p>{{ project.proj-description }}</p>
        </div>
    </main>
</template>