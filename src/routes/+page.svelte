<script>
    import {supabase} from '$lib/supabase';
    
    let promise = supabase.from("countries").select();
</script>

<div class ="prose">
<h1>Aufgaben</h1>

<ul><li>anstatt eines JS objects dass auf der seite ist, möchte ich eine liste aller länder</li>

<li>
    Bei Daisy UI ein loading symbol einbinden

</li>

<li>
    gib die vercel URL zum Projekt ab

</li>
</ul>
</div>

{#await promise}
    <p>Loading...</p>
{:then result}
  <div>{JSON.stringify(result)}</div>

  {/await}