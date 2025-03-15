<script lang="ts">
	import '../app.css';
	import SettingsPopover from '$lib/components/SettingsPopover.svelte';
	let { children } = $props();
</script>

<div>
	<!-- Top navigation bar -->
	<nav class="z-10 flex h-14 items-center justify-between px-4 sm:px-6">
		<div class="text-lg font-bold sm:text-xl">Portus</div>
		<button class="rounded-full p-2 transition-colors" aria-label="Settings">
			<SettingsPopover />
		</button>
	</nav>
	{@render children()}
</div>
