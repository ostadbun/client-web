<script lang="ts">
	import "../app.css";
	import favicon from "$lib/assets/icon.svg";
	import { ModeWatcher } from "mode-watcher";
	import Nav from "./components/Navbar/nav.svelte";
	import { page } from "$app/state";

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<title
		>استادبان{page.data.segmentTitle &&
			" | " + page.data.segmentTitle}</title
	>
</svelte:head>
<ModeWatcher />

<Nav />
{@render children()}
