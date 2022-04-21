<script>
  // variable
  let desc = ""

  // Reactive variable
  $: character = desc.length
  $: words = desc.split(" ").length

  // lebih dari 1 statement
  // $: {
  //   console.log("==========");
  //   console.log(`Description: ${desc}`)
  // }

  // condition if else
  $:  if (desc.length < 5) {
    console.log("KURANG dari 5");
  } else {
    console.log("==========");
    console.log(`Description: ${desc}`)
  }
</script>

<div>  
  <textarea bind:value={desc} name="" id="" cols="30" rows="10"></textarea>
  <p>{desc}</p>
  <p>Characters Count: {character}</p>
  <p>Words Count: {words}</p>
</div>

<style>
  div{
    margin-top: 1em;
    margin-bottom: 1em;
  }
</style>