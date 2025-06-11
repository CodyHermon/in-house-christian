<script>
	import { Button } from "$lib/components/ui/button";
	import { Card, CardContent, CardHeader, CardTitle } from "$lib/components/ui/card";
	import { FileText, Users, Droplet } from "@lucide/svelte";
</script>

<div class="container mx-auto px-4 py-8">
	<section class="max-w-6xl mx-auto">
		<div class="text-center mb-16">
			<h1 class="text-4xl md:text-5xl font-bold mb-4">Forms</h1>
			<div class="w-24 h-1 bg-primary mx-auto mb-6"></div>
			<p class="text-lg text-gray-600 max-w-2xl mx-auto">
				Download the forms you need for ministry participation, membership, and baptism.
			</p>
		</div>

		<!-- Forms Grid -->
		<div class="grid md:grid-cols-3 gap-8 mb-12">
			<!-- Ministry Permission Form -->
			<Card
				class="text-center hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2"
			>
				<CardHeader>
					<CardTitle class="text-xl">Ministry Permission</CardTitle>
				</CardHeader>
				<CardContent class="space-y-4">
					<div class="flex justify-center mb-4">
						<div
							class="w-16 h-16 bg-secondary/10 rounded-full flex items-center justify-center transition-transform duration-300"
						>
							<FileText class="w-8 h-8 text-secondary transition-transform duration-300" />
						</div>
					</div>
					<p class="text-gray-600">
						Required form for children and youth participating in KRIB, DIGS Jr., and DIGS
						ministries.
					</p>
					<Button
						href="/permission_form.pdf"
						target="_blank"
						rel="noopener noreferrer"
						class="w-full"
					>
						Download Form
					</Button>
				</CardContent>
			</Card>

			<!-- Membership Form -->
			<Card
				class="text-center hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2"
			>
				<CardHeader>
					<CardTitle class="text-xl">Membership</CardTitle>
				</CardHeader>
				<CardContent class="space-y-4">
					<div class="flex justify-center mb-4">
						<div
							class="w-16 h-16 bg-accent/10 rounded-full flex items-center justify-center transition-transform duration-300"
						>
							<Users class="w-8 h-8 text-accent transition-transform duration-300" />
						</div>
					</div>
					<p class="text-gray-600">
						Application form for those interested in becoming a member of In-House Christian
						Foursquare Church.
					</p>
					<Button
						href="/membership_form.pdf"
						target="_blank"
						rel="noopener noreferrer"
						class="w-full"
					>
						Download Form
					</Button>
				</CardContent>
			</Card>

			<!-- Water Baptism Form -->
			<Card
				class="text-center hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2"
			>
				<CardHeader>
					<CardTitle class="text-xl">Water Baptism</CardTitle>
				</CardHeader>
				<CardContent class="space-y-4">
					<div class="flex justify-center mb-4">
						<div
							class="w-16 h-16 bg-primary/10 rounded-full flex items-center justify-center transition-transform duration-300"
						>
							<Droplet class="w-8 h-8 text-primary transition-transform duration-300" />
						</div>
					</div>
					<p class="text-gray-600">
						Registration form for those who want to take the next step in their faith journey
						through baptism.
					</p>
					<Button
						href="/water_baptisim.pdf"
						target="_blank"
						rel="noopener noreferrer"
						class="w-full"
					>
						Download Form
					</Button>
				</CardContent>
			</Card>
		</div>

		<!-- Additional Information -->
		<div
			class="mt-16 text-center bg-gradient-to-r from-primary/5 to-primary/10 border-l-4 border-primary p-8 rounded-r-lg shadow-sm"
		>
			<h2 class="text-2xl font-semibold mb-4">Need Help?</h2>
			<p class="text-gray-600 mb-4">
				If you have questions about any of these forms or need assistance completing them, please
				don't hesitate to contact us.
			</p>
			<p class="text-primary font-semibold">Email: inhousechristian@gmail.com</p>
		</div>
	</section>
</div>

<style>
	.container {
		max-width: 1200px;
	}
</style>
