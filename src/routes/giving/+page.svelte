<script>
	import { Button } from "$lib/components/ui/button";
	import { Card, CardContent, CardHeader, CardTitle } from "$lib/components/ui/card";
	import { Mail, CreditCard } from "@lucide/svelte";
</script>

<div class="container mx-auto px-4 py-8 max-w-4xl">
	<div class="text-center">
		<!-- Header -->
		<div class="mb-16">
			<h1 class="text-4xl md:text-5xl font-bold mb-4">Online Giving</h1>
			<div class="w-24 h-1 bg-primary mx-auto mb-6"></div>
		</div>

		<!-- Scripture Quote -->
		<div class="bg-blue-50 border-l-4 border-primary p-6 mb-8 rounded-r-lg mx-auto">
			<p class="text-lg md:text-xl leading-relaxed italic mb-2">
				"Yes, you will be enriched in every way so that you can always be generous. And when we take
				your gifts to those who need them, they will thank God."
			</p>
			<p class="text-primary font-semibold text-sm">— 2 Corinthians 9:11</p>
		</div>

		<!-- Thank You Message -->
		<div class="mb-8">
			<p class="text-xl font-semibold text-gray-900 mb-4">Thank you for your generous giving!</p>
		</div>

		<!-- Giving Options -->
		<div class="grid md:grid-cols-2 gap-8 mb-8 mx-auto">
			<!-- E-transfer Option -->
			<Card class="hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2">
				<CardHeader>
					<div class="flex justify-center mb-4">
						<div class="w-16 h-16 bg-primary/10 rounded-full flex items-center justify-center">
							<Mail class="h-8 w-8 text-primary" />
						</div>
					</div>
					<CardTitle class="text-xl text-center">E-Transfer</CardTitle>
				</CardHeader>
				<CardContent class="text-center">
					<p class="mb-4 text-gray-600">Send your gift directly via email transfer</p>
					<p class="font-semibold text-primary text-lg">inhousegives@gmail.com</p>
				</CardContent>
			</Card>

			<!-- Online Option -->
			<Card class="hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2">
				<CardHeader>
					<div class="flex justify-center mb-4">
						<div class="w-16 h-16 bg-accent/10 rounded-full flex items-center justify-center">
							<CreditCard class="h-8 w-8 text-accent" />
						</div>
					</div>
					<CardTitle class="text-xl text-center">Online Platform</CardTitle>
				</CardHeader>
				<CardContent class="text-center">
					<p class="mb-4 text-gray-600">
						Secure online giving through our platform by clicking the button below
					</p>
				</CardContent>
			</Card>
		</div>

		<!-- Give Button -->
		<div class="mb-6">
			<Button
				href="https://checkout.square.site/merchant/6HSETNMKEPJJ4/checkout/NCQPJJZYOCYSY52UN6XG2SK3"
				target="_blank"
				rel="noopener noreferrer"
				class="text-xl px-12 py-4 h-auto"
				size="lg"
			>
				Give Now Online
			</Button>
		</div>
	</div>
</div>

<style>
	.container {
		max-width: 1200px;
	}
</style>
