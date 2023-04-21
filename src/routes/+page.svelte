<script lang="ts">
 
function displayText(){
	const explanation = document.getElementById("para") as HTMLParagraphElement;

	var getText = document.getElementById("content") as HTMLTextAreaElement;
	if(getText !== null){

		console.log(getText.value)
		explanation.textContent = getText.value;
	}
	
	
}


</script>



<form>
	<textarea id="content"rows="7" class="flex mx-auto w-[40%] " placeholder="hello?" on:input={()=>displayText()}></textarea>
	<button type="button" class="btn flex mx-auto  m-4 w-[40%] variant-filled-primary py-2" >Explain It</button>
	<div class="m-10">
		<h2 class="font-bold ml-40 text-left">Explanation:</h2>
		<p id="para"class="text-center"></p>
	</div>
</form>

