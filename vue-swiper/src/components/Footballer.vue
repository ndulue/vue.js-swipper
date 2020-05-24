<template>
    <div>
        <div class="movie" v-bind:style="{ backgroundImage: 'url('+ image +')'}">
            <div class="content">
                <h1 class="title">{{ title }}</h1>
                <p class="description">{{ description }} </p>
                <p class="description">{{ position }} </p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Movie',
    props : ['image', 'title', 'description', 'position'],
}
</script>

<style scoped>
    h1, h2, p {
      font-weight: normal;
      color: aliceblue;
    }
    .movie{
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: bottom;
      padding: 10px;
      width : 100%;
      height : 400px;
      background-repeat: no-repeat;
      background-blend-mode: overlay;
      background-size: cover;
    }
</style>