<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@shopware-pwa/composables](./composables.md) &gt; [useAddToCart](./composables.useaddtocart.md)

## useAddToCart variable

> This API is provided as a preview for developers and may change based on feedback that we receive. Do not use this API in a production environment.
> 

Add product to cart. Options - [IUseAddToCart](./composables.iuseaddtocart.md)

<b>Signature:</b>

```typescript
useAddToCart: (product: Product) => IUseAddToCart
```

## Example

Example of possibilities:

```ts
const {isInCart, quantity, addToCart} = useAddToCart(product)
if (!isInCart.value) {
   quantity.value = 5
   await addToCart()
}

```

