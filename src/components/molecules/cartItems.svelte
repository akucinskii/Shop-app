<script>
	export let item;
</script>

<div class="item__info">
	<div class="item__info--image">
		<img src={item.img} alt="zdjęcie produktu" />
	</div>
	<span>{item.product_name}</span>
	<span
		>{#if item.on_sale == null}{item.price}{:else}{(
				item.price -
				item.price * (item.on_sale / 100)
			).toFixed(2)}{/if} €</span
	>
</div>

<style>
	.item__info {
		width: 100%;
		display: grid;
		grid-template-columns: 1fr 5fr 1fr;
		gap: 15px 15px;
		grid-template-areas: '. . . .';
		align-items: center;
		border-bottom: 1px solid #d0d0d0;
	}
	.item__info--image {
		margin: 10px;
	}
	img {
		width: 100px;
		height: 100px;
		object-fit: cover;
		margin: auto;
	}
</style>
