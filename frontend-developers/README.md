# We're hiring Front-end Developers! 👨‍💻 👩‍💻

Don't hesitate to do the challenges presented here and tell us: jobs@conduktor.io!

We're hiring Front-end Developers experimented with React and Typescript, with an interest in beautiful UIs, able to think as a user (UX), and used to work with backend teams (Scala here).

More details: https://www.conduktor.io/jobs/

# The Challenge

## Build a mini-Conduktor

We'd like you to create a tiny version of our software where we could register/login (using Auth0), create/list clusters and topics, and fetch data in real-time.

This is a Front-end challenge: it should be friendly to use.

## Structure

You must create a front-end project using:

- React
- TypeScript
- We'll provide you an OpenAPI specification to work with
- Ant Design (or better) for the UI components

## Requirements

- We should be able to login/logout using an Auth0 integration, [checkout their documentation](https://auth0.com/docs/quickstart/spa/react/01-login), this will automatically provide the front-end a JWT with user information
- Display the name/picture from the JWT token in the application (with a logout menu)
- I should be able to create clusters & topics (see below for the contract)
- I should be able to switch the locale in the application without screen full-refresh
  - eg: English, French (or your native language!)
- If I open the application in multiple tabs: they must be synchronized
  - eg1: if I create a resource on tab A, I should see it on tab B
  - eg2: if I logout on tab A, it should logout my on tab B

## Contract sample

Here is a sample of the OpenAPI contract to get you an idea:

- `GET /clusters`: list the clusters
- `POST /clusters`: create a cluster
- `GET /clusters/:clusterId/topics`: list the topics of the cluster
- `POST /clusters/:clusterId/topics/:topic`: create a topic in this cluster
- `GET /clusters/:clusterId/topics/:topic/data`: you should generate random data here (to simulate a backend) websockets or SSE

We don't provide any backend server, you only have the OpenAPI specification to work with.

## How long?

Time estimated: it depends on you!

It's really the "job" at Conduktor, just think that it's your onboarding. :-)
