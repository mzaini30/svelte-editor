<hr>
<div>
	<button on:click|preventDefault={() => block('h1')} class="btn btn-success" >H1</button>
	<button on:click|preventDefault={() => block('h2')} class="btn btn-success">H2</button>
	<button on:click|preventDefault={() => block('h3')} class="btn btn-success">H3</button>
	<button on:click|preventDefault={() => block('h4')} class="btn btn-success">H4</button>
	<button on:click|preventDefault={() => block('p')} class="btn btn-success">P</button>
	<button on:click|preventDefault={() => sebagian('bold')} class="btn btn-success">Bold</button>
	<button on:click|preventDefault={() => sebagian('italic')} class="btn btn-success">Italic</button>
	<button on:click|preventDefault={() => link('createLink')} class="btn btn-success">Link</button>
	<button on:click|preventDefault={() => sebagian('unlink')} class="btn btn-success">Unlink</button>
	<button on:click|preventDefault={() => link('insertImage')} class="btn btn-success">Image</button>
	<button on:click|preventDefault={() => sebagian('insertOrderedList')} class="btn btn-success">List Number</button>
	<button on:click|preventDefault={() => sebagian('insertUnorderedList')} class="btn btn-success">List Bullet</button>
</div>
<hr>
<div contenteditable bind:innerHTML={html} style="max-height: {tinggi}" ></div>
<hr>

<script type="text/javascript">
	export let html
	export let tinggi = '78vh'
	function block(x){
		document.execCommand('formatBlock', false, x)
	}
	function sebagian(x){
		document.execCommand(x, false, null)
	}
	function link(x){
		const url = prompt('Masukkan linknya')
		document.execCommand(x, false, url)
	}
</script>

<style type="text/css">
	button {
		margin-bottom: 0.3em;
	}
	div {
		overflow: auto;
	}
</style>
