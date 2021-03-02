<script>
	import Editor from '@/Editor.svelte'
	let isinya
</script>

<div class="container py-3">
	<Editor bind:html={isinya} tinggi='50vh' ></Editor>
</div>