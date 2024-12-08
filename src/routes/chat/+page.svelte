<script>

	

	import { Card, Button, Toggle, Textarea, Alert, ToolbarButton } from 'flowbite-svelte';
	import { ArrowRightOutline, ImageOutline, FaceGrinOutline, PaperPlaneOutline } from 'flowbite-svelte-icons';

	import SelectionCard from "/src/lib/components/selectionCard.svelte";
	import ChatBubble from "/src/lib/components/chatBubble.svelte";
	
  </script>

<svelte:head>
	<title>Search</title>
	<meta name="description" content="About this app" />
</svelte:head>

<div class="mt-4">
	<h1 class="text-3xl font-semibold mb-2">Good Afternoon</h1>

	<p class="mb-6">
		Our AI Assistant will now guide you towards a fitting solution.
	</p>

	<div class="flex flex-col h-72 outline rounded outline-2 outline-gray-500 mb-2 p-4 overflow-y-scroll">
					
		
		 <ChatBubble imgsrc="/src/lib/images/robot-pfp.webp" name="AI Assistant" timestamp="just now" text="Hello! To find the best solution for you, I'd like to ask a couple of questions."/>

		 <ChatBubble imgsrc="/src/lib/images/robot-pfp.webp" name="AI Assistant" timestamp="just now" text="How many people do you plan to train on cybersecurity?"/>
	</div>

	<form>
		<label for="chat" class="sr-only">Your message</label>
		<div class="flex items-center px-3 py-2 rounded-lg bg-gray-50 dark:bg-gray-700">
		  <ToolbarButton color="dark" class="text-gray-500 dark:text-gray-400">
			<ImageOutline class="w-6 h-6" />
			<span class="sr-only">Upload image</span>
		  </ToolbarButton>
		  <ToolbarButton color="dark" class="text-gray-500 dark:text-gray-400">
			<FaceGrinOutline class="w-6 h-6" />
			<span class="sr-only">Add emoji</span>
		  </ToolbarButton>
		  <Textarea id="chat" class="mx-4 bg-white dark:bg-gray-800" rows="1" placeholder="Your message..." />
		  <ToolbarButton type="submit" color="blue" class="rounded-full text-primary-600 dark:text-primary-500">
			<PaperPlaneOutline class="w-6 h-6 rotate-45" />
			<span class="sr-only">Send message</span>
		  </ToolbarButton>
		</div>
	  </form>


</div>
