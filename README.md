---

# Prime Explorer

This application provides sample code that showcases the [Coinbase Prime APIs](https://docs.cloud.coinbase.com/prime/docs#introduction). The example UI that interacts with both the REST and WebSocket endpoints. The application was built using [Svelte](https://svelte.dev/), [Carbon Design System](https://carbondesignsystem.com/), and [TailWind CSS](https://tailwindcss.com/).

Requires [Node.js](https://nodejs.org) 16.x+

# Clone the git repo

```bash
git clone git@github.com:coinbase-samples/prime-explorer-js.git
```

## Getting started

Init via npm:

```bash
cd /primer-explorer-js
npm install
```

## Set Prime credentials

Navigate to your Prime Settings and pull your API credentials:

```bash
https://prime.coinbase.com/portfolio/{your_portfolio_id}/settings/address-book
```

Optionally, add Exchange API credentials (sandbox or prod):

```bash
https://public.sandbox.exchange.coinbase.com/profile/api
````

## Set environment variables

Add the following environment variables to an .env file in base of the repository:

```bash
PROD_SVC_ACCOUNTID=YOUR_SENDER_COMP_ID
PROD_ACCESS_KEY=YOUR_ACCESS_KEY
PROD_PORTFOLIO_ID=YOUR_PORTFOLIO_ID
PROD_PASSPHRASE=YOUR_PASSPHRASE
PROD_SIGNING_KEY=YOUR_SIGNING_KEY
PROD_URL=wss://ws-feed.prime.coinbase.com
PROD_API_HOST=https://api.prime.coinbase.com
PORT=YOUR_PORT
HTTP_HOST=http://localhost
ENTITY_ID=YOUR_ENTITY_ID
```
Validate the values in the .env file:

```bash
 source .env
 echo $PROD_SVC_ACCOUNTID
```

*Optional*

To test some of the Coinbase Exchange endpoints, add the following to the .env file:

```bash
EXCHANGE_PROD_ACCESS_KEY=YOUR_ACCESS_KEY
EXCHANGE_PROD_PASSPHRASE=YOUR_PASSPHRASE
EXCHANGE_PROD_SIGNING_KEY=YOUR_SIGNING_KEY
```

Run the application:

```bash
npm run dev
```

Navigate to [localhost:{{yourPort}}](http://localhost:{{yourPort}}). You should see the app running.


## Generate a build

Via CLI:

```bash
npm run build
```

Run the latest changes with `npm run start`. This app uses [sirv](https://github.com/lukeed/sirv), which is included in the dependencies, so that the app will work when you deploy to platforms like [Heroku](https://heroku.com).


