<script>
    import Card from "../Card.svelte";

    let cards = [
        { id: 1, title: "Card 1", description: "This is card 1" },
        { id: 2, title: "Card 2", description: "This is card 2" },
        { id: 3, title: "Card 3", description: "This is card 3" },
    ];

</script>
<header>
    <h1 class="bg-red-500">ecommerce/+page</h1>
</header>

<div class="flex flex-row gap-6 p-8">
    {#each cards as card}
        <Card id={card.id} title={card.title} description={card.description} />
    {/each}
</div>