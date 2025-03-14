<script lang="ts">
	import { i18n } from '$lib/i18n';
	import { ParaglideJS } from '@inlang/paraglide-sveltekit';
	import '../app.css';
	import SettingsPopover from '$lib/components/SettingsPopover.svelte';
	let { children } = $props();

	// document.documentElement.classList.toggle(
	// 	'dark',
	// 	localStorage.theme === 'dark' ||
	// 		(!('theme' in localStorage) && window.matchMedia('(prefers-color-scheme: dark)').matches)
	// );
	// // Whenever the user explicitly chooses light mode
	// localStorage.theme = 'dark';
	// // Whenever the user explicitly chooses dark mode
	// // localStorage.theme = 'dark';
	// // Whenever the user explicitly chooses to respect the OS preference
	// // localStorage.removeItem('theme');
</script>

<ParaglideJS {i18n}>
	<!-- Top navigation bar -->
	<nav class="z-10 flex h-14 items-center justify-between px-4 sm:px-6">
		<div class="text-lg font-bold sm:text-xl">Portus</div>
		<button class="rounded-full p-2 transition-colors" aria-label="Settings">
			<SettingsPopover />
		</button>
	</nav>
	{@render children()}
</ParaglideJS>
