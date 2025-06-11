<script>
	import {
		Card,
		CardContent,
		CardDescription,
		CardHeader,
		CardTitle
	} from "$lib/components/ui/card";
	import { Church, Mail, MapPin, School } from "@lucide/svelte";
</script>

<svelte:head>
	<title>Contact Us - In-House Christian Foursquare Church</title>
	<meta name="description" content="Get in touch with In-House Christian Foursquare Church. Find our service times, locations in Surrey BC, and contact information." />
</svelte:head>

<div class="container mx-auto px-4 py-8">
	<section class="max-w-6xl mx-auto">
		<div class="text-center mb-16">
			<h1 class="text-4xl md:text-5xl font-bold mb-4">Contact Us</h1>
			<div class="w-24 h-1 bg-primary mx-auto mb-6"></div>
			<p class="text-lg text-gray-600 max-w-2xl mx-auto">
				We'd love to hear from you! Get in touch with us or visit one of our service locations.
			</p>
		</div>

		<!-- Main Contact Info -->
		<div class="mb-12">
			<Card
				class="text-center hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2 max-w-md mx-auto"
			>
				<CardContent class="pt-6">
					<div class="flex justify-center mb-4">
						<div class="p-4 bg-primary/10 rounded-full">
							<Mail class="h-12 w-12 text-primary" />
						</div>
					</div>
					<CardTitle class="text-2xl mb-2">Get In Touch</CardTitle>
					<CardDescription>
						<strong>Email:</strong><br />
						<a
							href="mailto:inhousechristian@gmail.com"
							class="text-primary hover:text-primary/80 font-semibold transition-colors duration-300"
						>
							inhousechristian@gmail.com
						</a>
					</CardDescription>
				</CardContent>
			</Card>
		</div>

		<!-- Service Locations -->
		<div class="grid md:grid-cols-2 gap-8 mb-12">
			<Card
				class="text-center hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2"
			>
				<CardContent class="pt-6">
					<div class="flex justify-center mb-4">
						<div class="p-4 bg-primary/10 rounded-full">
							<School class="h-12 w-12 text-primary" />
						</div>
					</div>
					<CardTitle class="text-xl mb-2">Surrey Christian School</CardTitle>
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
						<strong>Service Time:</strong><br />
						Sunday: 4:00 PM
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
