<template>
    <div>
        <my-header></my-header>
        <b-container>
            <b-row>
                <b-col cols="9">我站九个</b-col>
                <b-col cols="3">我站三个</b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    import myHeader from '~/components/myHeader'
    export default {
        name: "index",
        components:{
            myHeader
        }
    }
</script>

<style>

</style>