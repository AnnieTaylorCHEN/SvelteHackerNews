<script>
    export let comment;
</script>

<style>
.container {
    padding: 5px 10px;
    margin-left: 25px;
    margin-top: 20px;
}

.html{
    border-bottom: 1px solid lightgray;    
}

</style>

{#each comment.comments as comment}
    <div class="container">
        <p>{comment.user} {comment.time_ago}</p> 
        <div class="html">
        {@html comment.content}
        </div>
        <svelte:self {comment} />
    </div>
{/each}