<script lang="ts">
	import type { Snippet } from 'svelte';

	let { sidebar, content }: { sidebar: Snippet; content: Snippet } = $props();
</script>

<div class="flex h-screen w-screen gap-4 bg-primary-surface p-4">
	<div class="flex flex-col items-center h-full w-xs rounded-3xl bg-primary-surface-raised p-4">
		{@render sidebar()}
	</div>
	<div class="h-full w-full p-4">
		{@render content()}
	</div>
</div>
