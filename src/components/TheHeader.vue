<template>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <a class="navbar-brand">
            <img src="../assets/logo.png" width="30" height="30"/>
        {{ title }}
        </a>
        <button class="navbar-toggler">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse">
            <ul class="navbar-nav">
                <li class="nav-item">
                    <a class="nav-link">Boutique</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link">Admin</a>
                </li>
            </ul>
        </div>
    </nav>

</template>

<script>
    export default {
        name: "theHeader",
        props : {
            title: {
                type: String,
                required: true,
            },
        }
    }
</script>

<style scoped>

</style>