<script>
	import { cartItems } from '../../stores/cartStore';
</script>

<a href="/cart" class="cart__button">
	<svg
		xmlns="http://www.w3.org/2000/svg"
		class="h-6 w-6"
		fill="none"
		viewBox="0 0 24 24"
		stroke="currentColor"
	>
		<path
			stroke-linecap="round"
			stroke-linejoin="round"
			stroke-width="2"
			d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z"
		/>
	</svg>
	<div class="cart_length">
		{$cartItems.length}
	</div>
</a>

<style>
	.cart__button {
		text-decoration: none;
		color: black;
		width: 40px;
		height: 40px;
		border: none;
		background: transparent;
	}
	.cart__button:hover {
		transition: all 0.3s;
		transform: scale(1.2);
		cursor: pointer;
	}
	.cart_length {
		position: absolute;
		top: 30px;
		background-color: orange;
		padding: 2px;
		font-size: 12px;
		width: 15px;
		height: 15px;
		text-align: center;
		border-radius: 100%;
	}
</style>
