<script lang="ts">
	// The ordering of these imports is critical to your app working properly
	import '@skeletonlabs/skeleton/themes/theme-crimson.css';
	// If you have source.organizeImports set to true in VSCode, then it will auto change this ordering
	import '@skeletonlabs/skeleton/styles/all.css';
	// Most of your app wide CSS should be put in this file
	import '../app.postcss';
	import { AppShell, LightSwitch } from '@skeletonlabs/skeleton';
</script>

<AppShell>
	<LightSwitch class="m-2" />

	<h1 class="text-center card font-bold py-5 mx-auto">Explain it like I'm Five</h1>

	<h3 class=" p-10 text-center" style="">Enter something you don't understand well</h3>

	<slot />
</AppShell>

<style>
	.card {
		width: 800px;
	}
</style>
