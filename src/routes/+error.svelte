<script>
	import { Button } from "$lib/components/ui/button";
	import { Card, CardContent } from "$lib/components/ui/card";
	import { page } from "$app/state";
	import { Home, ArrowLeft, Church } from "@lucide/svelte";

	// Get error details safely
	let status = $derived(page.status || 404);
	let message = $derived(page.error?.message || "Something went wrong");
</script>

<svelte:head>
	<title>{status} - In-House Christian Foursquare Church</title>
	<meta name="description" content="Page not found - In-House Christian Foursquare Church" />
</svelte:head>

<div class="container mx-auto px-4 py-16 max-w-4xl">
	<div class="min-h-[60vh] flex items-center justify-center">
		<Card class="w-full max-w-2xl text-center shadow-xl">
			<CardContent class="pt-16 pb-16">
				<!-- Error Icon -->
				<div class="flex justify-center mb-8">
					<div class="p-6 bg-primary/10 rounded-full">
						<Church class="h-16 w-16 text-primary" />
					</div>
				</div>

				<!-- Error Status -->
				<h1 class="text-4xl md:text-5xl font-bold mb-4">{status}</h1>

				<div class="w-24 h-1 bg-primary mx-auto mb-6"></div>

				<!-- Error Message -->
				{#if status === 404}
					<h2 class="text-2xl md:text-3xl font-bold mb-4">Page Not Found</h2>
					<p class="text-lg text-gray-600 mb-8 max-w-md mx-auto leading-relaxed">
						We're sorry, but the page you're looking for seems to have wandered off. Let us help you
						find your way back home.
					</p>
				{:else if status === 500}
					<h2 class="text-2xl md:text-3xl font-bold mb-4">Server Error</h2>
					<p class="text-lg text-gray-600 mb-8 max-w-md mx-auto leading-relaxed">
						We're experiencing some technical difficulties. Please try again in a moment.
					</p>
				{:else}
					<h2 class="text-2xl md:text-3xl font-bold mb-4">Oops!</h2>
					<p class="text-lg text-gray-600 mb-8 max-w-md mx-auto leading-relaxed">
						{message}
					</p>
				{/if}

				<!-- Scripture Verse -->
				<div class="bg-blue-50 border-l-4 border-primary p-6 mb-8 rounded-r-lg mx-auto max-w-lg">
					<p class="text-lg font-medium text-gray-800 italic mb-2">
						"Trust in the Lord with all your heart and lean not on your own understanding."
					</p>
					<p class="text-primary font-semibold">— Proverbs 3:5</p>
				</div>

				<!-- Action Buttons -->
				<div class="flex flex-col sm:flex-row gap-4 justify-center items-center">
					<Button
						href="/"
						size="lg"
						class="text-lg px-8 py-4 shadow-xl hover:shadow-2xl transition-all duration-300 transform hover:-translate-y-1"
					>
						<Home class="w-5 h-5 mr-2" />
						Go Home
					</Button>

					<Button
						variant="outline"
						size="lg"
						onclick={() => history.back()}
						class="text-lg px-8 py-4 shadow-lg hover:shadow-xl transition-all duration-300 transform hover:-translate-y-1"
					>
						<ArrowLeft class="w-5 h-5 mr-2" />
						Go Back
					</Button>
				</div>

				<!-- Additional Help -->
				<div class="mt-12 pt-8 border-t border-gray-200">
					<p class="text-gray-600 mb-4">Need help finding something?</p>
					<div class="flex flex-wrap justify-center gap-4 text-sm">
						<a href="/about" class="text-primary hover:underline">About Us</a>
						<a href="/ministries" class="text-primary hover:underline">Ministries</a>
						<a href="/giving" class="text-primary hover:underline">Giving</a>
						<a href="/contact" class="text-primary hover:underline">Contact</a>
					</div>
				</div>
			</CardContent>
		</Card>
	</div>
</div>

<style>
	.container {
		max-width: 1200px;
	}
</style>
