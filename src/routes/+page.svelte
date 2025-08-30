<script>
	import { Button } from "$lib/components/ui/button";
	import { Card, CardContent, CardDescription, CardTitle } from "$lib/components/ui/card";
	import OptimizedImage from "$lib/components/ui/OptimizedImage.svelte";
	import { School, Church, BookOpen } from "@lucide/svelte";
</script>

<svelte:head>
	<title>In-House Christian Foursquare Church - Bringing People to Jesus</title>
	<meta
		name="description"
		content="Welcome to In-House Christian Foursquare Church in Surrey, BC. Our mission is to bring our family, friends, and neighbours into a loving relationship with Jesus."
	/>
</svelte:head>

<!-- Hero Section -->
<section class="relative text-center py-16 min-h-screen overflow-hidden">
	<OptimizedImage
		src="/home.avif"
		alt="In-House Christian Foursquare Church - Beautiful church interior"
		class="absolute inset-0 w-full object-cover hero-image"
		skeletonClass="absolute inset-0 w-full hero-image"
		loading="eager"
		fetchpriority="high"
	/>
	<div
		class="absolute inset-0 bg-gradient-to-b from-black/50 via-black/70 to-black/80 hero-overlay"
	></div>
	<div
		class="relative z-10 container mx-auto px-4 flex flex-col justify-center items-center min-h-full"
	>
		<div class="max-w-4xl mx-auto text-center">
			<h1 class="text-5xl md:text-7xl font-bold text-white mb-6 leading-tight">
				Bringing People to Jesus
			</h1>
			<div class="w-24 h-1 bg-primary mx-auto mb-8"></div>
			<p class="text-lg md:text-xl text-gray-200 mb-10 max-w-3xl mx-auto leading-relaxed">
				At In-House our mission is to bring our family, friends, and neighbours into a loving
				relationship with Jesus by Receiving Jesus Christ as their Lord and Saviour, Elevating in
				Spiritual Maturity, Actively participating in ministry, Communicating God's message to the
				world and Honoring God in our life worship.
			</p>
			<div class="flex flex-col sm:flex-row gap-4 justify-center items-center">
				<Button
					size="lg"
					href="/Declaration_of_Faith.pdf"
					target="_blank"
					class="text-lg px-8 py-4 shadow-xl hover:shadow-2xl transition-all duration-300 transform hover:-translate-y-1"
				>
					What We Believe
				</Button>
			</div>
		</div>
	</div>
</section>

<div class="container mx-auto px-4">
	<!-- Video Section -->
	<section class="pt-16 bg-gray-50">
		<div class="max-w-4xl mx-auto">
			<div class="relative aspect-video rounded-lg overflow-hidden shadow-lg">
				<video class="w-full h-full object-cover" controls preload="metadata" poster="/home.avif">
					<source
						src="https://video.wixstatic.com/video/cac8c5_3ac6871cfc6e4ae382966aeaf22bf57c/1080p/mp4/file.mp4"
						type="video/mp4"
					/>
					<track kind="captions" src="" label="English" default />
					Your browser does not support the video tag.
				</video>
			</div>
		</div>
	</section>
</div>

<div class="container mx-auto px-4">
	<!-- Quick Info Cards -->
	<section class="grid md:grid-cols-3 gap-8 py-16">
		<Card
			class="text-center hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2"
		>
			<CardContent class="pt-6">
				<div class="flex justify-center mb-4">
					<div class="p-4 bg-primary/10 rounded-full">
						<School class="h-12 w-12 text-primary" />
					</div>
				</div>
				<CardTitle class="text-xl mb-2">Surrey Christian School (Primary Campus)</CardTitle>
				<CardDescription>
					8888 162 St<br />
					Surrey, BC V4N 3G1<br /><br />
					<strong>Service Time:</strong><br />
					Sunday: 10:15 AM
				</CardDescription>
			</CardContent>
		</Card>

		<Card
			class="text-center hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2"
		>
			<CardContent class="pt-6">
				<div class="flex justify-center mb-4">
					<div class="p-4 bg-destructive/10 rounded-full">
						<Church class="h-12 w-12 text-destructive" />
					</div>
				</div>
				<CardTitle class="text-xl mb-2">Cloverdale Building</CardTitle>
				<CardDescription>
					17665 66A Ave #412<br />
					Surrey, BC V3S 7X1<br /><br />
					<strong>Service Times:</strong><br />
					Sunday: 04:00 PM
				</CardDescription>
			</CardContent>
		</Card>

		<Card
			class="text-center hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2"
		>
			<CardContent class="pt-6">
				<div class="flex justify-center mb-4">
					<div class="p-4 bg-accent/10 rounded-full">
						<BookOpen class="h-12 w-12 text-accent" />
					</div>
				</div>
				<CardTitle class="text-xl mb-2">Weekly Ministries</CardTitle>
				<CardDescription>
					Mondays- Prayer Service<br />
					Wednesdays - KRIB (Children's Ministry)<br />
					Fridays - Food Distribution<br />
					Fridays- DIGS (Youth Ministry)
				</CardDescription>
			</CardContent>
		</Card>
	</section>
</div>

<style>
	.container {
		max-width: 1200px;
	}

	:global(.hero-image),
	.hero-overlay {
		height: calc(100vh - 80px);
	}
</style>
