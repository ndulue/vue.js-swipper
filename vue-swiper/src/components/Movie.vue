<template>
    <div>
        <div class="movie" v-bind:style="{ backgroundImage: 'url('+ image +')'}">
            <div class="content">
                <h1 class="title">{{ title }}</h1>
                <p class="description">{{ description }} </p>
                <p class="description">{{ duration }} </p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Movie',
    props : ['image', 'title', 'description', 'duration'],
}
</script>

<style scoped>
    h1, h2 {
      font-weight: normal;
    }
    .movie{
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      justify-content: flex-end;
      text-align: left;
      padding: 10px;
      width : 350px;
      height : 500px;
      background-color: rgba(255,255,255,0.7);
      background-repeat: no-repeat;
      background-blend-mode: overlay;
      background-size: cover;
    }
</style>