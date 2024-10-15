<script>
	import { cartCount } from '$lib/stores/cartStore.js';

    export let id
    export let title
    export let description

</script>


<div class="w-40 h-60 border border-blue-500">
    <h1 class="text-2xl">{id}</h1>
    <h1 class="text-2xl">{title}</h1>
    <p class="text-lg">{description}</p>
    <button on:click="{() => {
        //aquí verificamos si el carrito está vacío y le colocamos directamente el numero 1
        if(!$cartCount){
            cartCount.set(1)
            //si el carrito no está vacío, le sumamos 1
        } else {
            cartCount.update((n) => n + 1);
        }
         }}"  class="bg-blue-500 text-white">Click me</button>
</div>