<script>
import { fade } from 'svelte/transition'
import { Link } from 'svelte-routing'
export let id, title, points, user, time_ago, comments_count,url, index;
</script>

<style>
    article {
        padding: 5px 10px;
        margin: 15px;
        background: lightcyan;
        border-radius: 10px;
    }
</style>

<article in:fade={{delay: 50 * index}}>
    <h2>
        <a href={url}>{title}</a>
    </h2>
    <p> {points} points by {user} {time_ago}</p>
    <Link to={`/item/${id}`}> {comments_count} comments </Link>
</article>
