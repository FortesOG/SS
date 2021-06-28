<template>
    <li>
        <span v-bind:class="{done: info.complited}">
            
            <strong>{{info.id}}</strong>
            {{info.title}}

        </span>
        
        <button class="rm" v-on:click="$ ('go-to',info.id)">
            &times;
        </button>
    </li>
</template>

<script>
export default {
    props:{
        info :
        {
            type: Object,
            required: true
        }
    }
}
</script>

<style  scoped>

li{
    border: 1px solid #ccc;
    display: flex;
    justify-content: space-between;
    padding: .5rem 2rem;
    margin-bottom: 1rem;
}
input
{
    margin-right: 1rem;
}

.rm
{ 
    background: greenyellow;
    color: #fff;
    border-radius: 50%;
    font-weight: bold;


}

.done
{
    text-decoration: red;

}


</style>