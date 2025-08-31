<script lang="ts">
	import { Skeleton } from "$lib/components/ui/skeleton";
	import { onMount } from "svelte";

	interface Props {
		src: string;
		alt: string;
		class?: string;
		skeletonClass?: string;
		loading?: "lazy" | "eager";
		fetchpriority?: "high" | "low" | "auto";
		sizes?: string;
		width?: number;
		height?: number;
	}

	let {
		src,
		alt,
		class: className = "",
		skeletonClass = "",
		loading = "lazy",
		fetchpriority = "auto",
		sizes,
		width,
		height,
		...restProps
	}: Props = $props();

	let imageLoaded = $state(false);
	let imageError = $state(false);
	let imgElement: HTMLImageElement;

	function handleLoad() {
		// Use requestAnimationFrame to avoid forced reflow
		requestAnimationFrame(() => {
			imageLoaded = true;
		});
	}

	function handleError() {
		imageError = true;
		imageLoaded = true; // Hide skeleton even on error
	}

	// Preload critical images
	onMount(() => {
		if (loading === "eager" || fetchpriority === "high") {
			const img = new Image();
			img.onload = handleLoad;
			img.onerror = handleError;
			img.src = src;
		}
	});
</script>

<!-- Skeleton placeholder -->
{#if !imageLoaded}
	<Skeleton class={`${className} ${skeletonClass}`} />
{/if}

{#if imageLoaded}
	<!-- Actual image -->
	<img
		bind:this={imgElement}
		{src}
		{alt}
		{loading}
		{fetchpriority}
		{sizes}
		{width}
		{height}
		class={`${className} ${imageLoaded ? "opacity-100" : "opacity-0"} transition-opacity duration-300`}
		onload={handleLoad}
		onerror={handleError}
		{...restProps}
	/>
{/if}

{#if imageError}
	<div class={`${className} bg-gray-100 flex items-center justify-center text-gray-400`}>
		<svg class="w-8 h-8" fill="currentColor" viewBox="0 0 20 20">
			<path
				fill-rule="evenodd"
				d="M4 3a2 2 0 00-2 2v10a2 2 0 002 2h12a2 2 0 002-2V5a2 2 0 00-2-2H4zm12 12H4l4-8 3 6 2-4 3 6z"
				clip-rule="evenodd"
			/>
		</svg>
	</div>
{/if}
