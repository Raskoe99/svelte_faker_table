<script>
    import TableHead from '../tableHead/TableHead.svelte';
    import People from '../people/People.svelte'

    function range(start, end) {
        return Array(end - start + 1).fill().map((_, idx) => start + idx)
    }
    
    var result = range(1, 2);

    const personTable = [
        "1",
        "2",
        "3",
        "4",
        "5"
    ]
</script>

<div>
    <table>
        <thead>
            <TableHead/>
        </thead>
        <tbody>
            {#each personTable as person}
                <People/>
            {/each}
        </tbody>
    </table>  
</div>


<style>
    div{
        width: 100%;
    }
    table {
        border: 3px solid black;
        text-align: center;
        float: none;
        margin: 0 auto;
        width: 75%;
        border-collapse: collapse;
    }
</style>