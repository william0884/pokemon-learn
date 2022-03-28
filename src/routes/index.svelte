
<script>
  import {pokemon, fetchPokemon} from "../stores/pokestore";
  import {onMount} from "svelte";
  console.log($pokemon)
  onMount(() => {
    fetchPokemon();
  });

</script>
<svelte:head>
<title>First Life</title>
</svelte:head>

<h1 class="text-4xl text-center my-8">First Life</h1>

{#if $pokemon != null}
{#each $pokemon as pokeman}

<p>{pokeman.name}</p>
{/each}
{/if}
