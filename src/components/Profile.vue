<template>
    <div>
        <h2>Profile</h2>
        <h3>Profile: {{ userId }} </h3>
    </div>
</template>

<script>
    export default {
        name: 'Profile',
        data(){
            return {
                userId: this.$route.params.userId,
            }
        },
        methods:{
            updateId(){
                this.userId = this.$route.params.userId
            }
        },
        watch: {
            $route: 'updateId'
        }
    }
</script>

<style scoped>

</style>