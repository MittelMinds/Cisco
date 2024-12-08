<script>
    export let imgsrc;
    export let name;
    export let timestamp;
    export let text;
</script>

<div class="flex items-start gap-2.5 mb-4">
    <img class="w-10 h-10 rounded-full" src={imgsrc} alt="pfp">
    <div class="flex flex-col w-full max-w-[320px] leading-1.5 p-4 border-gray-200 bg-gray-100 rounded-e-xl rounded-es-xl dark:bg-gray-700">
       <div class="flex items-center space-x-2 rtl:space-x-reverse">
          <span class="text-sm font-semibold text-gray-900 dark:text-white">{name}</span>
          <span class="text-sm font-normal text-gray-500 dark:text-gray-400">{timestamp}</span>
       </div>
       <p class="text-sm font-normal py-2.5 text-gray-900 dark:text-white">{text}</p>
    </div>		
</div>