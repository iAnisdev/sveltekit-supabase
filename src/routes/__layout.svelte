<script>
    import {onMount} from 'svelte'
import supabase from "$lib/supabase";


async function createuser(){
    // Create a new user
    const { user, error } = await supabase.auth.signUp({
    email: 'example@email.com',
    password: 'example-password',
    })
    console.log(error)
    console.log(user)
}
// onMount(createuser())
</script>

<slot></slot>