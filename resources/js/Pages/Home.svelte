<script>
    let step = 0;

    let inputs = [
        {
            type: 'text',
            name: 'Name'
        },
        {
            type: 'number',
            name: 'Phone Number'
        },
        {
            type: 'email',
            name: 'Email'
        }
    ]

    function next(){
        step += 1;
    }
 </script>

<div>
    {#each inputs as input, i}
        {#if i <= step }
            <label>{ input.name }</label>
            <input type="{input.type}"/>
            <br>
        {/if}
    {/each}
    <button on:click={next}>Continue</button>

</div>