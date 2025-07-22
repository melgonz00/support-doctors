<script>
    let { children } = $props();
</script>

<div class="article-text">
    <p>
        {@render children()}
    </p>
</div>

<style>
    .article-text {
        margin: 50vh auto;
        width: 90%;
        background-color: #000000;
        color: #ffffff;
        border: solid #000000 3px;
        border-radius: 20px;
        padding: 20px;
        box-shadow: 16px 16px #000000;
        font-size: x-large;
    }
</style>
