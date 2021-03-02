# Svelte Editor

## Instalasi

```bash
npm i svelte-editor
```

## Menggunakan

```html
<script type="text/javascript">
	let isinya = `<strong>Hello</strong>`
	import Editor from 'svelte-editor'
</script>

<Editor bind:html={isinya}/>
```

## Parameter Opsional

**tinggi** (default: 78vh)

Untuk menentukan maksimal tinggi editor.

Contoh:

```html
<Editor bind:html={isinya} tinggi='50vh'/>
```

## Contoh Jadinya

![](https://i.ibb.co/rF4mh02/image.png)

![](https://i.ibb.co/hXJvpqS/image.png)