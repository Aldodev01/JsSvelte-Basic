<script>
	import EmojiDIsplay from "./emojiDIsplay.svelte";
	import EmojiDesctription from "./emojiDescription.svelte"


	let emoji = "🥳"
	const emojis = ["☠️", "👽", "🤖", "👾"]


	// membuat random emoji menggunakan Math.random
	const randomizeEmoji = () => {
		return emojis[Math.floor(Math.random() * emojis.length)]
	}

	// menjalankan function random emoji
	const handlerandom = () => {
		emoji = randomizeEmoji()
	}

	// Variable yang dibuat untuk loading
	let isLoaded = false
	// Kondisi yang digunakan untuk mengganti loading ke trues
	setTimeout(() => {
		isLoaded = true
	}, 2000);
</script>

<div>
	<h1>Randomize EMoji</h1>
	<!-- Looping dengan each -->
<ul>
	{#each emojis as emoji}
	<li>
		{emoji}
	</li>
	{/each}
</ul>

<!-- Kondisi didalam html -->
	{#if isLoaded === true }
	<EmojiDIsplay {emoji}/>
	<EmojiDesctription /> 
	<button on:click={handlerandom}> Random</button>
	{:else}
	<h2>loading ...</h2>
	{/if}
</div>

<style>
	button{
		background-color: blue;
		color: aliceblue;
		padding: 0.75em;
		border-radius: 0.25em;
		border: 1px solid salmon;
		box-shadow: 0.4rem 0.4rem 0 #222;
	}
	button:hover{
		box-shadow: 0.25em 0.25em 0 #222;
		transition: all 0.4s ease 0s;
		background-color: rgb(57, 57, 240);

	}
	div{
		margin: 2em;
	}
	:global(p) {
		color: crimson;
	}
</style>