## GQL Server

Run :

`node ./index.js`

- Server listens at http://localhost:4000/graphql

- Subscription server listens at [ws://localhost:4000/subscriptions](ws://localhost:4000/subscriptions)

You can use https://studio.apollographql.com/sandbox/explorer?overlay=connection-settings to explore the API, just fill in the two endpoints above

## Flaky mode

Same API, but with 10% error chances on API calls

Run :

`node ./index.js --flaky`
