<script>
  export let emoji
	// let currentEmoji = "😁";
	//  setTimeout(() => {
	// 	currentEmoji = "😛"
	//  }, 2000); 

  let currentButton = "button1"
</script>

<div> 
  <p>ALDO</p> {emoji}
  <button 
    class={currentButton === "button1" ? "active" : "asede"} 
    on:click={() => (currentButton = "button1")}
  >
    button 1
  </button>
  <button  
    class={currentButton === "button2" ? "active" : "asede"} 
    on:click={() => (currentButton = "button2")}
  >
    button 2
  </button>
  <button  
    class={currentButton === "button3" ? "active" : "asede"} 
    on:click={() => (currentButton = "button3")}
  >
    button 3
  </button>
</div>

<style>
  div{
    font-size: 3em;
    margin-bottom: 0.5em;
  }
  button{
    color: aqua;
    background-color: blue;
  }
  .active{
    background-color: aqua;
    color: blue;
  }
</style>