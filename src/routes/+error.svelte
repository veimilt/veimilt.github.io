<script>
    import { page } from "$app/state";
</script>

<div>
    <p>{page.status}: {page.error.message}</p>
    <a href="/">Etusivulle</a>
</div>

<style>
    div {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 500px;
        gap: 0.5rem;
        background-color: var(--bg-primary);
    }
    p {
        color: var(--text-subtle);
        font-size: 2rem;
        margin-bottom: 0;
        font-weight: bold;
    }

    a:hover {
        text-decoration: underline;
    }
</style>
