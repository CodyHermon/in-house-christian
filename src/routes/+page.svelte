<script>
	import { Button } from "$lib/components/ui/button";
	import { Card, CardContent, CardDescription, CardTitle } from "$lib/components/ui/card";
	import { School, Church, BookOpen } from "@lucide/svelte";
</script>

<!-- Hero Section -->
<section
	class="text-center py-16 bg-cover bg-top bg-no-repeat relative min-h-screen"
	style="background-image: url('home.jpg');"
>
	<div class="absolute inset-0 bg-black/70"></div>
	<div
		class="relative z-10 container mx-auto px-4 flex flex-col justify-start items-center min-h-screen pt-32"
	>
		<h1 class="text-4xl md:text-6xl font-bold text-white mb-6">Bringing People to Jesus...</h1>
		<p class="text-xl text-gray-200 mb-8 max-w-2xl mx-auto text-left">
			At In-House our mission is to bring our family, friends, and neighbours into a loving
			relationship with Jesus by Receiving Jesus Christ as their Lord and Saviour, Elevating in
			Spiritual Maturity, Actively participating in ministry, Communicating God's message to the
			world and Honoring God in our life worship.
		</p>
		<div class="space-x-4">
			<Button size="lg" href="/Declaration_of_Faith.pdf" target="_blank">What We Believe</Button>
		</div>
	</div>
</section>

<!-- Video Section -->
<section class="py-16 bg-gray-50">
	<div class="max-w-4xl mx-auto">
		<div class="relative aspect-video rounded-lg overflow-hidden shadow-lg">
			<video class="w-full h-full object-cover" controls preload="metadata" poster="/home.jpg">
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

<div class="container mx-auto px-4">
	<!-- Quick Info Cards -->
	<section class="grid md:grid-cols-3 gap-8 py-16">
		<Card class="text-center">
			<CardContent class="pt-6">
				<div class="flex justify-center mb-4">
					<School class="h-12 w-12 text-primary" />
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

		<Card class="text-center">
			<CardContent class="pt-6">
				<div class="flex justify-center mb-4">
					<Church class="h-12 w-12 text-destructive" />
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

		<Card class="text-center">
			<CardContent class="pt-6">
				<div class="flex justify-center mb-4">
					<BookOpen class="h-12 w-12 text-accent" />
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
</style>
