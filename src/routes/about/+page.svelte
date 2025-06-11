<script>
	import { Card, CardContent, CardDescription, CardTitle } from "$lib/components/ui/card";
	import OptimizedImage from "$lib/components/ui/OptimizedImage.svelte";
</script>

<div class="container mx-auto px-4 py-8">
	<section class="max-w-6xl mx-auto">
		<div class="text-center mb-16">
			<h1 class="text-4xl md:text-5xl font-bold mb-4">Our Team</h1>
			<div class="w-24 h-1 bg-primary mx-auto mb-6"></div>
			<p class="text-lg text-gray-600 max-w-2xl mx-auto">Get to know us!</p>
		</div>
		<div class="grid md:grid-cols-2 gap-8">
			<Card
				class="text-center hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2 group"
			>
				<CardContent class="pt-8">
					<div
						class="w-48 h-48 mx-auto mb-6 rounded-full overflow-hidden border-4 border-primary shadow-lg group-hover:border-primary/80 transition-all duration-300"
					>
						<OptimizedImage
							src="/val.avif"
							alt="Pastor Val Batulan"
							class="w-full h-full object-cover transition-transform duration-300 group-hover:scale-105"
							fetchpriority="high"
							loading="eager"
						/>
					</div>
					<CardTitle class="text-2xl mb-2">Pastor Val Batulan</CardTitle>
					<CardDescription class="text-primary font-medium mb-2">Lead Pastor</CardDescription>
					<CardDescription class="text-sm text-left">
						It was always in Pastor Val's heart to plant a church and in 2006, God opened doors for
						that to happen. Pastor Val graduated as a civil engineer in the Philippines and when he
						migrated to Canada, he graduated from Life Bible College which is now formally known as
						Pacific Life Bible College. Prior to starting In-House, he served as an assistant pastor
						at Kingsway Foursquare Church.
						<br />
						<br />
						He is married to his wife, Maricar, who is a registered nurse. Together, they have 3 children.
					</CardDescription>
				</CardContent>
			</Card>

			<Card
				class="text-center hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2 group"
			>
				<CardContent class="pt-8">
					<div
						class="w-48 h-48 mx-auto mb-6 rounded-full overflow-hidden border-4 border-primary shadow-lg group-hover:border-primary/80 transition-all duration-300"
					>
						<OptimizedImage
							src="/harrison.avif"
							alt="Pastor Harrison Pride"
							class="w-full h-full object-cover transition-transform duration-300 group-hover:scale-105"
						/>
					</div>
					<CardTitle class="text-2xl mb-2">Pastor Harrison Pride</CardTitle>
					<CardDescription class="text-primary font-medium mb-2">Associate Pastor</CardDescription>
					<CardDescription class="text-sm text-left">
						Pastor Harrison has his bachelor's degree in pastoral leadership from Pacific Life Bible
						College. Right now, he is focusing on serving in the areas of missions, young adults,
						and sharing the gospel. Him and his wife, Zian, have two daughters, Zemi and Alaya.
						<br />
						<br />
						"It always brings me joy to partner with my family, friends, and neighbors on their faith
						journey wherever they are at and bring them closer to God."
					</CardDescription>
				</CardContent>
			</Card>

			<Card
				class="text-center hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2 group"
			>
				<CardContent class="pt-8">
					<div
						class="w-48 h-48 mx-auto mb-6 rounded-full overflow-hidden border-4 border-primary shadow-lg group-hover:border-primary/80 transition-all duration-300"
					>
						<OptimizedImage
							src="/youlein.avif"
							alt="Pastor Youlein Bajarias"
							class="w-full h-full object-cover transition-transform duration-300 group-hover:scale-105"
						/>
					</div>
					<CardTitle class="text-2xl mb-2">Pastor Youlein Bajarias</CardTitle>
					<CardDescription class="text-primary font-medium mb-2">Associate Pastor</CardDescription>
					<CardDescription class="text-sm text-left">
						Youlein currently serves as the worship pastor and children's coordinator for their
						Friday night kids ministry. She has been serving at In-House since their doors opened in
						2006.
						<br />
						<br />
						Youlein and her husband, Papen, have three boys: Zachari, Oziah, and Ezekiah.
						<br />
						<br />
						"What axcites me is seeing God's people coming together to worhip. I love serving alongside
						the people of In-House!"
					</CardDescription>
				</CardContent>
			</Card>

			<Card
				class="text-center hover:shadow-xl transition-all duration-300 transform hover:-translate-y-2 group"
			>
				<CardContent class="pt-8">
					<div
						class="w-48 h-48 mx-auto mb-6 rounded-full overflow-hidden border-4 border-primary shadow-lg group-hover:border-primary/80 transition-all duration-300"
					>
						<OptimizedImage
							src="/jhun.avif"
							alt="Pastor Jhun Agarpao"
							class="w-full h-full object-cover transition-transform duration-300 group-hover:scale-105"
						/>
					</div>
					<CardTitle class="text-2xl mb-2">Pastor Jhun Agarpao</CardTitle>
					<CardDescription class="text-primary font-medium mb-2"
						>Prince George Campus Pastor</CardDescription
					>
					<CardDescription class="text-sm text-left">
						Pastor Jhun was born and raised in the province of Cagayan, Philippines. He finished his
						bachelor's degree in theology at the Foursquare College in Manila, Philippines and thus
						dedicated his life for the work of the Lord since 1991. He also had the opportunity to
						facilitate 3 church plants in the Philippines before coming to Canada. Right now he is
						the Prince George Campus Pastor. He is married to his wife, Marie, and together they
						have 4 boys.
						<br />
						<br />
						"God has called me to start a new life here in Canada through the ministry of In-House Christian
						Foursquare Church.
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
