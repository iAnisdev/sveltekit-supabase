
<script>
    import supabase from "$lib/supabase";

    let name = ''
    async function addRecord(){
        const new_record = await supabase.from('users').insert({name: name })

        console.log("new_record " , new_record)
    }
</script>
<input type="text" bind:value={name} placeholder="Enter name">
<br />
<br />
<input type="button" value="Submit" on:click={addRecord}>const ne