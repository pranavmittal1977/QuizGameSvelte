<!-- <script lang="ts">
  import { goto } from "$app/navigation";
</script>

<h1>Welcome to SvelteKit</h1>
<button on:click={() => goto('/about') }>Go to About</button>

<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p> -->




<script lang="ts">
    import { createEventDispatcher } from 'svelte';
    import { goto } from "$app/navigation";

    let name = '';
    let age = '';
    let major = '';
  
    const dispatch = createEventDispatcher();
</script>
  
<main>
    <h1>Enter Your Details</h1>
    
    <form>
        <div>
            <label for="name">Name:</label>
            <input type="text" id="name" bind:value={name} required />
        </div>
        <div>
            <label for="age">Age:</label>
            <input type="number" id="age" bind:value={age} required />
        </div>
        <div>
            <label for="major">Major:</label>
            <input type="text" id="major" bind:value={major} required />
        </div>
        
        <button type="button" on:click={() => goto('/about') }>Go to About</button>
    </form>
</main>
  
<style>
    main {
        padding: 2em;
        max-width: 600px;
        margin: 0 auto;
        background: linear-gradient(135deg, #f5f5f5 0%, #e0e0e0 100%);
        border-radius: 10px;
        box-shadow: 0 6px 12px rgba(0, 0, 0, 0.1);
    }

    h1 {
        font-size: 2.2em;
        font-weight: 700;
        margin-bottom: 1.5em;
        color: #333;
        text-align: center;
    }

    form {
        display: flex;
        flex-direction: column;
        gap: 1.2em;
    }

    div {
        display: flex;
        flex-direction: column;
    }

    label {
        font-size: 1.2em;
        margin-bottom: 0.5em;
        color: #444;
    }

    input {
        padding: 0.8em;
        font-size: 1em;
        border: 1px solid #ccc;
        border-radius: 5px;
        background: #fff;
        color: #333;
        transition: border-color 0.3s ease, box-shadow 0.3s ease;
    }

    input:focus {
        border-color: #007bff;
        outline: none;
        box-shadow: 0 0 5px rgba(38, 143, 255, 0.3);
    }

    button {
        padding: 0.8em 1.6em;
        font-size: 1.2em;
        color: #fff;
        background-color: #007bff;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        transition: background-color 0.3s ease, transform 0.2s ease;
    }

    button:hover {
        background-color: #0056b3;
    }

    button:focus {
        outline: none;
        box-shadow: 0 0 0 3px rgba(38, 143, 255, 0.5);
    }

    button:active {
        transform: scale(0.98);
    }
</style>





<!--    
   <script lang="ts">
    import { goto } from "$app/navigation";
    let name = '';
    let age = '';
    let major = '';
</script>

<main class="p-8 max-w-md mx-auto bg-gray-100 rounded-lg shadow-md">
    <h1 class="text-3xl font-semibold mb-4 text-gray-800">Enter Your Details</h1>
    <div class="space-y-4">
        <div>
            <label for="name" class="block text-lg font-medium text-gray-600">Name:</label>
            <input type="text" id="name" bind:value={name} required class="mt-1 p-2 border border-gray-300 rounded-md w-full focus:outline-none focus:ring-2 focus:ring-blue-500" />
        </div>
        <div>
            <label for="age" class="block text-lg font-medium text-gray-600">Age:</label>
            <input type="number" id="age" bind:value={age} required class="mt-1 p-2 border border-gray-300 rounded-md w-full focus:outline-none focus:ring-2 focus:ring-blue-500" />
        </div>
        <div>
            <label for="major" class="block text-lg font-medium text-gray-600">Major:</label>
            <input type="text" id="major" bind:value={major} required class="mt-1 p-2 border border-gray-300 rounded-md w-full focus:outline-none focus:ring-2 focus:ring-blue-500" />
        </div>
        <div class="flex justify-center">
            <button on:click={() => goto('/about')} class="mt-4 py-2 px-6 bg-blue-500 text-blue-100 rounded-md shadow-sm focus:outline-blue-500 focus:ring-2 focus:ring-blue-400">
                Go to About
            </button>
        </div>
    </div>
</main> -->
