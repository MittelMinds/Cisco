<script>
	let chatStep = 0;


	function sendChat() {
        chatStep++;
        return chatStep;
    }


	import { Card, Button, Toggle, Textarea, Alert, ToolbarButton, GradientButton } from 'flowbite-svelte';
	import {
		ArrowRightOutline,
		ImageOutline,
		FaceGrinOutline,
		PaperPlaneOutline,
		GlobeOutline
	} from 'flowbite-svelte-icons';

	import SelectionCard from '/src/lib/components/selectionCard.svelte';
	import ChatBubble from '/src/lib/components/chatBubble.svelte';
</script>

<svelte:head>
	<title>Search</title>
	<meta name="description" content="About this app" />
</svelte:head>

<div class="">
	<h1 class="mb-2 text-3xl font-semibold">General Chat</h1>

	<p class="mb-6">Ask away.</p>

	<div 
		class="mb-2 flex h-80 flex-col overflow-y-scroll rounded p-4 outline outline-2 outline-gray-500"
	>
		<ChatBubble
			imgsrc="/src/lib/images/robot-pfp.webp"
			name="AI Assistant"
			timestamp="just now"
			text="Hello there! How may I help?"
		/>

		

	</div>

	<form>
		<label for="chat" class="sr-only">Your message</label>
		<div class="flex items-center rounded-lg bg-gray-50 px-3 py-2 dark:bg-gray-700">
			<ToolbarButton color="dark" class="text-gray-500 dark:text-gray-400">
				<GlobeOutline class="h-6 w-6" />
				<span class="sr-only">Change Language</span>
			</ToolbarButton>
			<Textarea
				id="chat"
				class="mx-4 bg-white dark:bg-gray-800"
				rows="1"
				placeholder="Your message..."
			/>
			<ToolbarButton
				on:click={sendChat}
				type="submit"
				color="blue"
				class="rounded-full text-primary-600 dark:text-primary-500"
			>
				<PaperPlaneOutline class="h-6 w-6 rotate-45" />
				<span class="sr-only">Send message</span>
			</ToolbarButton>
		</div>
	</form>
</div>
