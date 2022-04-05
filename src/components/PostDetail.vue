<template class="card">

<div class="card">
  <b-card
    title="Quote Title"
    img-src="https://picsum.photos/600/300/?image=25"
    img-alt="Image"
    img-top
    tag="article"
    style="max-width: 20rem;"
    class="mb-2"
  >
    <h3>
    {{id}}. {{title}}
    </h3>
    <p>{{body}}</p>
    <b-button href="#" variant="primary">Go somewhere</b-button>
  </b-card>
 
</div>
    
</template>

<script>
export default {
    name: "PostDetail",
    props: ['id', 'title', 'body'],

}
</script>

<style scoped>
    .card {
        display: flex-wrap;
        flex-direction: center;
        justify-content: space-between;
        align-self: stretch;
        margin-bottom: 10px;
    }

</style>