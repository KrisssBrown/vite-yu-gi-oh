<template>
    <div>

    </div>
</template>

<script>
import axios from 'axios'

import Card from './Card.vue' 

    export default {
        components:{
            Card
        },
        
        data() {
            return {
                
            }
        },

        methods: {
            fetchCard(){
                axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php').then((res)=>{
                    
                })
            }
        },

        mounted() {
            
        },

    }
</script>

<style lang="scss" scoped>

</style>