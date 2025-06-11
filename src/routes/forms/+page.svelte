<script>
	import { Button } from "$lib/components/ui/button";

	// Sample events data - in a real app, this would come from a database
	const upcomingEvents = [
		{
			id: 1,
			title: "Easter Sunday Celebration",
			date: "April 7, 2025",
			time: "9:00 AM & 11:00 AM",
			description: "Join us for a special Easter celebration with music, message, and fellowship.",
			location: "Main Sanctuary"
		},
		{
			id: 2,
			title: "Community Food Drive",
			date: "April 15, 2025",
			time: "10:00 AM - 2:00 PM",
			description: "Help us collect food donations for local families in need.",
			location: "Church Parking Lot"
		},
		{
			id: 3,
			title: "Youth Group Movie Night",
			date: "April 20, 2025",
			time: "6:00 PM - 9:00 PM",
			description: "Fun movie night for our youth group (ages 13-18) with snacks and fellowship.",
			location: "Youth Room"
		}
	];

	const recurringEvents = [
		{
			title: "Bible Study Groups",
			schedule: "Every Tuesday, 7:00 PM",
			description: "Small group Bible studies meeting in various locations"
		},
		{
			title: "Prayer Meeting",
			schedule: "Every Friday, 6:00 AM",
			description: "Early morning prayer meeting in the chapel"
		},
		{
			title: "Women's Fellowship",
			schedule: "First Saturday of each month, 10:00 AM",
			description: "Fellowship and encouragement for women of all ages"
		}
	];
</script>

<div class="container mx-auto px-4 py-8">
	<section class="max-w-6xl mx-auto">
		<h1 class="text-4xl font-bold text-gray-900 mb-8 text-center">Upcoming Events</h1>

		<!-- Upcoming Events -->
		<section class="mb-12">
			<h2 class="text-2xl font-semibold mb-6">Special Events</h2>
			<div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
				{#each upcomingEvents as event}
					<div
						class="bg-white border border-gray-200 rounded-lg p-6 shadow-sm hover:shadow-md transition-shadow"
					>
						<h3 class="text-xl font-semibold mb-2">{event.title}</h3>
						<div class="text-gray-600 space-y-1 mb-4">
							<p><strong>Date:</strong> {event.date}</p>
							<p><strong>Time:</strong> {event.time}</p>
							<p><strong>Location:</strong> {event.location}</p>
						</div>
						<p class="text-gray-700 mb-4">{event.description}</p>
						<Button variant="outline" size="sm">Learn More</Button>
					</div>
				{/each}
			</div>
		</section>

		<!-- Recurring Events -->
		<section class="mb-12">
			<h2 class="text-2xl font-semibold mb-6">Regular Activities</h2>
			<div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
				{#each recurringEvents as event}
					<div class="bg-blue-50 border border-blue-200 rounded-lg p-6">
						<h3 class="text-xl font-semibold mb-2">{event.title}</h3>
						<p class="text-blue-700 font-medium mb-2">{event.schedule}</p>
						<p class="text-gray-700">{event.description}</p>
					</div>
				{/each}
			</div>
		</section>

		<!-- Calendar Section -->
		<section class="bg-gray-50 p-8 rounded-lg">
			<h2 class="text-2xl font-semibold mb-4 text-center">Stay Connected</h2>
			<div class="text-center">
				<p class="text-gray-600 mb-6">
					Want to stay up to date with all our events and activities? Subscribe to our newsletter or
					follow us on social media.
				</p>
				<div class="space-x-4">
					<Button>Subscribe to Newsletter</Button>
					<Button variant="outline">View Full Calendar</Button>
				</div>
			</div>
		</section>
	</section>
</div>

<style>
	.container {
		max-width: 1200px;
	}
</style>
