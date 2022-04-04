<template>
    <h3>
    {{id}}. {{title}}
    </h3>
    <h5>{{body}}</h5>
</template>






<script>
export default {
    name: "PostDetail",
    props: ['id', 'title', 'body'],

    created(){
        console.log(this.id)
    }
}
</script>

