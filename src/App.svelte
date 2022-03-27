<script>
	import Hello from "./Welcome.svelte";
	import Test from "./Test.svelte"
	let userinput;
	let userresponse;
</script>

<style>
	main {
    font-family: sans-serif;
    text-align: center;
  }
	
  #output {
    color: red;
    font-size: 24px;
  }
</style>

<main>
	<Hello onValueChange="{(x) => userresponse = x}" username={userinput}/>
	<input bind:value={userinput}  placeholder="enter your name" />

	<p hidden id="output">
		Your response: <strong>{userresponse}</strong>
	</p>
</main>
