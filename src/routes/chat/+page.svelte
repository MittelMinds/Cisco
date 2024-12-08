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

<div class="mt-4">
	<h1 class="mb-2 text-3xl font-semibold">Good Afternoon</h1>

	<p class="mb-6">Our AI Assistant will now guide you towards a fitting solution.</p>

	<div 
		class="mb-2 flex h-72 flex-col overflow-y-scroll rounded p-4 outline outline-2 outline-gray-500"
	>
		<ChatBubble
			imgsrc="/src/lib/images/robot-pfp.webp"
			name="AI Assistant"
			timestamp="just now"
			text="Hello! To find the best solution for you, I'd like to ask a couple of questions."
		/>

		<ChatBubble
			imgsrc="/src/lib/images/robot-pfp.webp"
			name="AI Assistant"
			timestamp="just now"
			text="How many people do you plan to train on cybersecurity?"
		/>

		{#if chatStep>0}
			<ChatBubble
				imgsrc="/src/lib/images/cat-avatar.png"
				name="You"
				timestamp="just now"
				text="24"
			/>
		{/if}

		{#if chatStep>0}
			<ChatBubble
				imgsrc="/src/lib/images/robot-pfp.webp"
				name="AI Assistant"
				timestamp="just now"
				text="Great, thank you! Would you like the training to take place online, in person, or are you flexible?"
			/>
		{/if}

		{#if chatStep>1}
			<ChatBubble
				imgsrc="/src/lib/images/cat-avatar.png"
				name="You"
				timestamp="just now"
				text="I would prefer an in-person training session, but I am flexible, depending on cost. "
			/>
		{/if}


		{#if chatStep>1}
			<ChatBubble
				imgsrc="/src/lib/images/robot-pfp.webp"
				name="AI Assistant"
				timestamp="just now"
				text="All right, thanks. In which city is your company located?"
			/>
		{/if}

		{#if chatStep>2}
			<ChatBubble
				imgsrc="/src/lib/images/cat-avatar.png"
				name="You"
				timestamp="just now"
				text="We are in Munich."
			/>
		{/if}

		{#if chatStep>2}
			<ChatBubble
				imgsrc="/src/lib/images/robot-pfp.webp"
				name="AI Assistant"
				timestamp="just now"
				text="Thank you. Would you like the training session to be hosted in German, English, or perhaps a different language?"
			/>
		{/if}

		{#if chatStep>3}
			<ChatBubble
				imgsrc="/src/lib/images/cat-avatar.png"
				name="You"
				timestamp="just now"
				text="English would be best."
			/>
		{/if}

		{#if chatStep>3}
			<ChatBubble
				imgsrc="/src/lib/images/robot-pfp.webp"
				name="AI Assistant"
				timestamp="just now"
				text="Perfect, now I just have one last question: When would you like the training to take place? If you are flexible on the dates, feel free to tell me that too!"
			/>
		{/if}

		{#if chatStep>4}
			<ChatBubble
				imgsrc="/src/lib/images/cat-avatar.png"
				name="You"
				timestamp="just now"
				text="Something around the end of February next year, before noon, would be great."
			/>
		{/if}

		{#if chatStep>4}
			<ChatBubble
				imgsrc="/src/lib/images/robot-pfp.webp"
				name="AI Assistant"
				timestamp="just now"
				text="Perfect, thank you for taking the time to answer these questions. Is there anything else you'd like to tell me?"
			/>
		{/if}

		{#if chatStep>5}
			<ChatBubble
				imgsrc="/src/lib/images/cat-avatar.png"
				name="You"
				timestamp="just now"
				text="No, that's all."
			/>
		{/if}

		{#if chatStep>5}
			<ChatBubble
				imgsrc="/src/lib/images/robot-pfp.webp"
				name="AI Assistant"
				timestamp="just now"
				text="Please press next to continue to a page where you can view suitable options for your training. Have a nice day!"
			/>
		{/if}


		{#if chatStep>5}
			<GradientButton href="selection" class="ml-12 max-w-[320px]" color="purple">Next</GradientButton>
		{/if}

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
