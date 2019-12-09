<script>
import Headline from './../components/Headline.svelte';
let promise = fetch("https://node-hnapi.herokuapp.com/news?page=1").then(res => res.json());
</script>

{#await promise}
<h2>Loading...</h2>
{:then data}
    {#each data as headline, index}
    <Headline {...headline} {index} />
    {/each}
{/await}