<script lang="ts">
 let url = "https://api.funtranslations.com/translate/minion.json";
function displayText(){
	var explanation = document.getElementById("displaying") as HTMLParagraphElement;

	var getText = document.getElementById("content") as HTMLTextAreaElement;
	if(getText !== null){

		console.log(getText.value)
		explanation.textContent = getText.value;
	}
	
	
}

function translateToMinion(){
	var explanation = document.getElementById("displaying") as HTMLParagraphElement;
	var getText = document.getElementById("content") as HTMLTextAreaElement;
	var newUrl = `${url}?text=${getText.value}`;
	fetch(newUrl).then((response)=>response.json()).then((data)=>{
		console.log(data)
		explanation.textContent = data.contents.translated;
		console.log(data.contents.translated)
	})
}

</script>



<form>
	<textarea id="content"rows="7" class="flex mx-auto w-[40%] " placeholder="hello?" on:input={()=>displayText()}></textarea>
	<button type="button" class="btn flex mx-auto  m-4 w-[40%] variant-filled-primary py-2" on:click={()=>translateToMinion()}>Mnionssss</button>
	<div class="m-10">
		<h2 class="font-bold ml-40 text-left">Minions Translation:</h2>
		<p id="displaying"class="text-center"></p>
		
	</div>
	
</form>

