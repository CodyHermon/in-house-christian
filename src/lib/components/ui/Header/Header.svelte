<script lang="ts">
	import { Button } from "$lib/components/ui/button";
	import { Sheet, SheetContent, SheetTrigger } from "$lib/components/ui/sheet";
	import { page } from "$app/state";
	import { Menu } from "@lucide/svelte";

	const navigation = [
		{ name: "Home", href: "/" },
		{ name: "About", href: "/about" },
		{ name: "Ministries", href: "/ministries" },
		{ name: "Devotionals", href: "/devotionals" },
		{ name: "Giving", href: "/giving" },
		{ name: "Forms", href: "/forms" },
		{ name: "Contact", href: "/contact" }
	];

	let mobileMenuOpen = false;

	function closeMobileMenu() {
		mobileMenuOpen = false;
	}
</script>

<header class="sticky top-0 z-50 bg-white shadow-sm border-b">
	<div class="container mx-auto px-4 sm:px-6 lg:px-8">
		<div class="flex justify-between items-center h-20 py-4">
			<div class="flex items-center flex-1 min-w-0">
				<a href="/" class="flex items-center space-x-3">
					<img
						src="/favicon.png"
						alt="Grace Community Church Logo"
						class="h-14 w-14 flex-shrink-0"
					/>
					<div class="text-lg lg:text-xl font-bold font-heading hidden min-[300px]:block">
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
							{page.url.pathname === item.href ? 'text-primary border-b-2 border-primary' : ''}"
					>
						{item.name}
					</a>
				{/each}
			</nav>

			<!-- Mobile Sheet Menu -->
			<div class="lg:hidden flex-shrink-0">
				<Sheet bind:open={mobileMenuOpen}>
					<SheetTrigger
						class="p-2 hover:text-primary hover:bg-transparent rounded-md transition-colors"
					>
						<Menu class="h-6 w-6" />
						<span class="sr-only">Open menu</span>
					</SheetTrigger>
					<SheetContent side="right" class="w-[300px] sm:w-[350px]">
						<div class="flex flex-col h-full">
							<nav class="flex flex-col space-y-2 mt-12 flex-1">
								{#each navigation as item}
									<a
										href={item.href}
										on:click={closeMobileMenu}
										class="text-lg font-medium text-gray-900 hover:text-primary transition-colors duration-200 font-heading py-3 px-4 rounded-md
											{page.url.pathname === item.href ? 'text-primary bg-primary/10' : 'hover:bg-gray-50'}"
									>
										{item.name}
									</a>
								{/each}
							</nav>
						</div>
					</SheetContent>
				</Sheet>
			</div>
		</div>

		<!-- Remove the old mobile navigation that was pushing content down -->
	</div>
</header>

<style>
	.container {
		max-width: 1200px;
	}
</style>
