<script>
	import { School, Church } from "@lucide/svelte";
</script>

<!-- Footer -->
<footer class="bg-gray-900 text-white py-12">
	<div class="container mx-auto px-4">
		<div class="grid md:grid-cols-2 gap-16">
			<!-- Contact Info -->
			<div>
				<h3 class="text-xl font-bold mb-4">Contact Us</h3>
				<div class="space-y-2">
					<p class="flex items-center gap-2">
						<School class="h-4 w-4" />
						Surrey Christian School: 8888 162 St, Surrey, BC V4N 3G1
					</p>
					<p class="flex items-center gap-2">
						<Church class="h-4 w-4" />
						Cloverdale Building: 17665 66A Ave #412, Surrey, BC V3S 7X1
					</p>
					<p>
						Email: <a
							href="mailto:inhousechristian@gmail.com"
							class="hover:text-gray-300 transition-colors underline">inhousechristian@gmail.com</a
						>
					</p>
				</div>
			</div>

			<!-- Quick Links -->
			<div>
				<h3 class="text-xl font-bold mb-4">Quick Links</h3>
				<div class="space-y-2">
					<a href="/about" class="block hover:text-gray-300 transition-colors">About Us</a>
					<a href="/ministries" class="block hover:text-gray-300 transition-colors">Ministries</a>
					<a href="/events" class="block hover:text-gray-300 transition-colors">Devotionals</a>
					<a href="/giving" class="block hover:text-gray-300 transition-colors">Giving</a>
					<a href="/events" class="block hover:text-gray-300 transition-colors">Forms</a>
					<a href="/contact" class="block hover:text-gray-300 transition-colors">Contact</a>
				</div>
			</div>
		</div>

		<!-- Bottom Bar -->
		<div class="border-t border-gray-700 mt-8 pt-8 text-center">
			<p>&copy; 2025 In-House Christian Foursquare Church. All rights reserved.</p>
		</div>
	</div>
</footer>

<style>
	.container {
		max-width: 1200px;
	}
</style>
