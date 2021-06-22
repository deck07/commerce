# Next.js Commerce
This app uses Next.js Commerce
The all-in-one starter kit for high-performance e-commerce sites. With a few clicks, Next.js developers can clone, deploy and fully customize their own store.
Start right now at [nextjs.org/commerce](https://nextjs.org/commerce)

Demo live at: [aosapplicationtest-deck07.vercel.app](https://aosapplicationtest-deck07.vercel.app)

## Features
Aside from the default installation of Next.js ecommerce
- Randomized product catalog at front end
- Modification of built-in template

## Integrations

Backend ecommerce deployment:[store-xjhp7ifs5f.mybigcommerce.com](https://store-xjhp7ifs5f.mybigcommerce.com)

  Note: Inaccessible publicly using its default storefront. This is only used as headless server.

Client (public facing app):[aosapplicationtest-deck07.vercel.app](https://aosapplicationtest-deck07.vercel.app)

All configured using vercel setup wizard. Vercel automatically configured api keys. Could also be done if already bigcommerce store already exist. API keys should be generated manually.

Integration with local setup was configured using [vercel cli](https://vercel.com/cli)

  Run command: 
  
  vercel env pull .env.local

## Software used in running
node v16.3.0

npm v7.15.1

yarn v1.22.10

## How to run locally
yarn install

yarn run dev
 

##  Solution and Further Considerations
A. Randomization

  There's no apparent randomization in the backend catalogue,therefore the randomization has been implemented in the frontend, particularly right after resolving the product Promise.
  See [commit](https://github.com/deck07/commerce/commit/5926071e3c7975cf3582a19f06e0fdce067d5bd6)
  
Since the sandbox bigcommerce store has only 13 products in total, it was all used in populating the the frontpage.
Shall the store have sizeable number of products, it must only use a subset of the products to be randomized.
Possible solution with this scenario is to create logical category which groups the products that are allowed to be in the frontpage. The api query of this app in the frontpage should then be filtered with this category.



B. Layout/UI Changes

  The UI changes are for demonstration purposes only. Given limited time, and no particular design to implement yet the modification are more on colouring and "eye-candy" factor only.
  See [commit](https://github.com/deck07/commerce/commit/384fe68ed2241a0e2fb2ba392d5ca205e8b2d777)


