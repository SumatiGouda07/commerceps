# Payload E-Commerce Template

This is the official [Payload E-Commerce Template](https://github.com/payloadcms/payload/blob/main/templates/ecommerce). Use it to power e-commerce businesses and online stores of all sizes. This repo includes a fully-working backend, enterprise-grade admin panel, and a beautifully designed, production-ready website.

This template is right for you if you are selling:

- Physical products like clothing or merchandise
- Digital assets like ebooks or videos
- Access to content like courses or premium articles

Core features:

- Pre-configured Payload Config(how-it-works)
- Authentication(users-authentication)
- Access Control
- Shopping Cart
- Checkout
- Paywall 
- Layout Builder
- SEO
- Website


## Stripe

Payload itself handles no currency exchange. All payments are processed and billed using [Stripe](https://stripe.com). This means you must have access to a Stripe account via an API key, see [Connect Stripe](#connect-stripe) for how to get one. When you create a product in Payload that you wish to sell, it must be connected to a Stripe product by selecting one from the field in the product's sidebar, see [Products](#products) for more details. Once set, data is automatically synced between the two platforms in the following ways:

1. Stripe to Payload using [Stripe Webhooks](https://stripe.com/docs/webhooks):
   - `product.created`
   - `product.updated`
   - `price.updated`

1. Payload to Stripe using [Payload Hooks](https://payloadcms.com/docs/hooks/overview):
   - `user.create`

For more details on how to extend this functionality, see the the official [Payload Stripe Plugin](https://github.com/payloadcms/plugin-stripe).
