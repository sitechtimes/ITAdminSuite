<script lang="ts">
</script>

<div class="flex h-screen w-screen gap-4 bg-primary-surface p-4">
	<div class="h-full w-xs rounded-3xl bg-primary-surface-raised">
		<slot name="sidebar"></slot>
	</div>
	<div class="h-full flex-3 bg-yellow-500">
		<slot name="content"></slot>
	</div>
</div>
