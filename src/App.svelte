

<script>
	let top = 50;
	let left = 50;
	// up = 38
	// down = 40
	// right = 39
	// left = 37
	function onKeyDown(e) {
		 switch(e.keyCode) {
             case 87 :
                   if (top>=50){
                     top -= 50;
                   }
                   break;
             case 83:
                   if (top<=400){
                     top += 50;
                   }
                   break;
             case 65:
                  if (left>=50){
                     left -= 50;
                   }

                   break;
             case 68:
                   if (left<=400){
                     left += 50;
                   }

                   break;
		 }
         // console.log(e.keyCode)
	}

</script>
<style>
	main {
		width: 500px;
		height: 500px;
		border: solid blue 1px;
		margin: 10px auto;
		position: relative
	}
	div {
		width: 50px;
		height: 50px;
		background-color: green;
		position: absolute;
	}
</style>


<main>
	<div style="left: {left}px; top: {top}px">
	</div>
</main>

<svelte:window on:keydown|preventDefault={onKeyDown} />