<template>
    <div class="home">
        <router-link class="champ" :to="`/`" tag="div"><img src="@/assets/border.png" alt="border champ" width="100%" height="100%"></router-link>
        <router-link class="champ" :to="`/`" tag="div"><img src="@/assets/border.png" alt="border champ" width="100%" height="100%"></router-link>
        
        <h1 class="title">
            Nom : {{ nom }}
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
.home {
    display: flex;
}

.champ {
    position: relative;
    width: 10%;
    height: 10%;
}

.title {
    font-size: 24px;
    font-weight: 600;
}
</style>
