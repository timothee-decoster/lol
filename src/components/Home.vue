<template>
    <div>
        <router-link :to="`/`" tag="div"><img src="@/assets/border.png" alt="border champ" width="10%" height="10%"></router-link>
        <router-link :to="`/`" tag="div"><img src="@/assets/border.png" alt="border champ" width="10%" height="10%"></router-link>
        
        <h1 class="title">
            Nom : <pre>{{ nom }}</pre>
        </h1>
    </div>
</template>

<script>
export default {
    name: 'Home',
    data() {
        return {
            nom: this.$_GET('nom')
        };
    },
    methods: {
        $_GET(param) {
            var vars = {};
            window.location.href.replace(location.hash, '').replace(/[?&]+([^=&]+)=?([^&]*)?/gi, function(m, key, value) {
                vars[key] = value !== undefined ? value : '';
            });
            if (param) {
                return vars[param] ? vars[param] : null;
            }
            return vars;
        }
    }
};
</script>

<style>
.title {
    font-size: 24px;
    font-weight: 600;
}
</style>
