<script>
	import Header from '$lib/components/Header.svelte';
	import Button from '$lib/components/Button.svelte';
	import SidebarView from '$lib/components/SidebarView.svelte';
</script>

<SidebarView>
	{#snippet sidebar()}
		<Header label="SITHS Print Server" level={3} color="primary"></Header>
		<Button label="?" size="xl" color="primary"></Button>
		<Button label="?" size="xl" color="primary"></Button>
		<Button label="?" size="xl" color="primary"></Button>
	{/snippet}
	{#snippet content()}
		Random Text
	{/snippet}
</SidebarView>
