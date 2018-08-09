<template>
    <div class="zap-slideout" :class="{ isOpen: isOpen }">
        <div class="zap-slideout-opener" @click="toggle">Filtre</div>
        <form method="get">
            <input type="text" id="nom" name="nom" required>
            <button type="submit" value="Submit">chercher</button>
        </form>
        <button @click="reset">Supprimer recherche</button>
    </div>
</template>

<script>
export default {
    name: 'Sidebar',
    data: () => ({
        isOpen: false
    }),
    methods: {
        toggle() {
            this.isOpen = !this.isOpen;
        },
        reset() {
            window.location.href = window.location.href.split('?')[0];
        }
    }
};
</script>

<style>
.zap-slideout {
    position: relative;
    width: 240px;
    padding: 30px;
    background-color: #34495e;
    transform: translateX(-100%);
    transition: transform 0.6s;
}

.zap-slideout.isOpen {
    transform: translateX(0);
}

.zap-slideout-opener {
    position: absolute;
    top: 20px;
    left: 100%;
    margin-left: 20px;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.08em;
    color: #fff;
    cursor: pointer;
}

.zap-slideout-opener:hover {
    text-decoration: underline;
}
</style>
