<script lang="ts">
	import { Button } from "$lib/components/ui/button";
	import { page } from "$app/stores";

	const navigation = [
		{ name: "Home", href: "/" },
		{ name: "About", href: "/about" },
		{ name: "Ministries", href: "/ministries" },
		{ name: "Devotionals", href: "/devotionals" },
		{ name: "Giving", href: "/giving" },
		{ name: "Forms", href: "/forms" },
		{ name: "Contact", href: "/contact" }
	];
</script>

<header class="sticky top-0 z-50 bg-white shadow-sm border-b">
	<div class="container mx-auto px-4 sm:px-6 lg:px-8">
		<div class="flex justify-between items-center h-20 py-4">
			<!-- Logo/Church Name -->
			<div class="flex items-center flex-1 min-w-0">
				<a href="/" class="flex items-center space-x-3">
					<img
						src="/favicon.png"
						alt="Grace Community Church Logo"
						class="h-14 w-14 flex-shrink-0"
					/>
					<div class="text-lg lg:text-xl font-bold text-gray-900 font-heading">
						In-House Christian Foursquare Church
					</div>
				</a>
			</div>

			<!-- Desktop Navigation -->
			<nav class="hidden lg:flex space-x-6 xl:space-x-2 flex-shrink-0">
				{#each navigation as item}
					<a
						href={item.href}
						class="text-gray-700 font-bold hover:text-primary px-3 py-2 text-sm transition-colors duration-200 font-heading
							{$page.url.pathname === item.href ? 'text-primary border-b-2 border-primary' : ''}"
					>
						{item.name}
					</a>
				{/each}
			</nav>

			<!-- Mobile menu button -->
			<div class="lg:hidden flex-shrink-0">
				<Button variant="ghost" size="sm" class="p-2">
					<svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M4 6h16M4 12h16M4 18h16"
						/>
					</svg>
				</Button>
			</div>
		</div>

		<!-- Mobile Navigation (you can expand this later with a toggle) -->
		<div class="lg:hidden">
			<div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
				{#each navigation as item}
					<a
						href={item.href}
						class="text-gray-700 hover:text-primary block px-3 py-2 text-base font-medium font-heading
							{$page.url.pathname === item.href ? 'text-primary bg-primary/10' : ''}"
					>
						{item.name}
					</a>
				{/each}
			</div>
		</div>
	</div>
</header>

<style>
	.container {
		max-width: 1200px;
	}
</style>
