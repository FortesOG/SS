<template>
    <div>
        <ul>
            <LisLig 
                v-for="info of pageinfo"
                v-bind:info="info"
                v-on:go-to="goToo"
            />
        </ul>
    </div>
</template>

<script>
import LisLig from '@/components/LisLig.vue'

export default {
    props: ['pageinfo'],
    components :
    {
        LisLig
    },
    methods:
    {
        goToo(id)
        {
            this.$emit('goToo',id)

        }
    }
    
}
</script>

<style scoped>
ul
{
list-style: none;
margin: 0;
padding: 0;
}

</style>

