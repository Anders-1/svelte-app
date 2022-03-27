<script>
	export let username = "bob";
	
  export let onValueChange;
  let value;
  $: onValueChange(value);
	
	function smart(name) {
		document.getElementById("output").hidden = false;
		value = prompt("Is " + name + " smart?");
		if (value.toLowerCase() == "yes") {
			alert("You said " + name + " is smart");
		} else if (value.toLowerCase() == "no") {
			alert("You said " + name + " isn't smart");
		} else {
			alert("I dont know what you mean.");
		}
	}
</script>

<h1>Hello {username}</h1>
<button on:click={() => smart(username)}>Smart?</button>
