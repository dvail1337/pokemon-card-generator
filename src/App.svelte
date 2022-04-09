<script>
    import PokemonCard from "./PokemonCard.svelte";
</script>

<div class="wrapper">
    <img class="h1" src="./title.png.png" alt="wtf" />
    <img class="h2" src="./title-descript.png" alt="wtf" />
    <PokemonCard />
</div>

<style>
    .wrapper {
        display: flex;
        flex-direction: column;
        background-image: url(/background-jig.jpg);
        background-size: 100%;
        background-repeat: no-repeat;
        height: 100%;
        width: 100%;
        align-items: center;
    }
    .h1 {
        max-width: 500px;
        margin-top: 30px;
        margin-bottom: 0;
    }
    .h2 {
        max-width: 500px;
        margin-top: 10px;
        margin-bottom: 70px;
    }
</style>
