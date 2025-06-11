<script>
	import { Card, CardContent, CardDescription, CardTitle } from "$lib/components/ui/card";
	import OptimizedImage from "$lib/components/ui/OptimizedImage.svelte";
</script>

<svelte:head>
	<title>Ministries - In-House Christian Foursquare Church</title>
	<meta name="description" content="Discover our ministries at In-House Christian Foursquare Church including worship services, children's ministry, youth programs, and community outreach." />
</svelte:head>

<div class="container mx-auto px-4 py-8">
	<section class="max-w-6xl mx-auto">
		<div class="text-center mb-16">
			<h1 class="text-4xl md:text-5xl font-bold mb-4">Ministries</h1>
			<div class="w-24 h-1 bg-primary mx-auto mb-6"></div>
			<p class="text-lg text-gray-600 max-w-2xl mx-auto">
				At In-House we have ministries for all ages!
			</p>
		</div>

		<!-- Ministry Cards Grid -->
		<div class="grid md:grid-cols-2 gap-8 mb-12">
			<Card
				class="overflow-hidden hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2 group"
			>
				<div class="aspect-video overflow-hidden">
					<OptimizedImage
						src="/ministries_1.avif"
						alt="KRIB"
						class="w-full h-full object-cover object-top"
						fetchpriority="high"
						loading="eager"
					/>
				</div>
				<CardContent class="p-6">
					<CardTitle class="text-2xl mb-3">KRIB (Children's Ministry)</CardTitle>
					<CardDescription class="mb-4">
						We are back! We meet at the church building from 5:30 PM to 7:00 PM. We hope to see you
						this Friday!
					</CardDescription>
					<p><strong>When:</strong> Fridays</p>
					<p><strong>Ages:</strong> 5 - 11 years old</p>
				</CardContent>
			</Card>

			<!-- DIGS (Youth Ministry) -->
			<Card
				class="overflow-hidden hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2 group"
			>
				<div class="aspect-video overflow-hidden">
					<OptimizedImage
						src="/ministries_2.avif"
						alt="DIGS"
						class="w-full h-full object-cover object-top"
					/>
				</div>
				<CardContent class="p-6">
					<CardTitle class="text-2xl mb-3">DIGS Jr. / DIGS</CardTitle>
					<CardDescription class="mb-4">
						Our DIGS Jr. and DIGS program are geared for teens! Not only do you learn about how much
						God loves you, but you do so through fun and exciting activities!
					</CardDescription>
					<p><strong>Ages:</strong> 12-18 years</p>
				</CardContent>
			</Card>

			<!-- Young Adults -->
			<Card
				class="overflow-hidden hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2 group"
			>
				<div class="aspect-video overflow-hidden">
					<OptimizedImage
						src="/ministries_3.avif"
						alt="Young Adults"
						class="w-full h-full object-cover object-top"
					/>
				</div>
				<CardContent class="p-6">
					<CardTitle class="text-2xl mb-3">Young Adults</CardTitle>
					<CardDescription class="mb-4">
						Life can be busy, especialy for a young adult! Our young adults ministry is a great way
						to meet new and old friends and just find refreshment in the word of God!
					</CardDescription>
					<p><strong>Ages:</strong> College and Career</p>
				</CardContent>
			</Card>

			<!-- Ladies Night -->
			<Card
				class="overflow-hidden hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2 group"
			>
				<div class="aspect-video overflow-hidden">
					<OptimizedImage
						src="/ministries_4.avif"
						alt="Ladies Night Ministry"
						class="w-full h-full object-cover object-center"
					/>
				</div>
				<CardContent class="p-6">
					<CardTitle class="text-2xl mb-3">Ladies Night</CardTitle>
					<CardDescription class="mb-4">
						A special time for women to come together for fellowship, encouragement, and spiritual
						growth. We share stories, pray for one another, and build meaningful friendships while
						studying God's word together.
					</CardDescription>
				</CardContent>
			</Card>
		</div>
	</section>
</div>

<style>
	.container {
		max-width: 1200px;
	}
</style>
