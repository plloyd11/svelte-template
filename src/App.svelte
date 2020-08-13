<script>
    import Header from './ui/Header.svelte'
    let count = 0
    let addShit = () => {
        count++
    }
    $: console.log(`${count}`)
    let list = [1,2,3,4]
</script>

<main>
    <Header />
    <p>{count}</p>
    <button on:click={addShit}>Add Shit!</button>
    <ul class="flex">
        {#each list as item}
            <li>{item}</li>
        {/each}
    </ul>
</main>
