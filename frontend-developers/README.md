# We're hiring Front-end Developers! 👨‍💻 👩‍💻

Don't hesitate to do the challenges presented here and tell us: jobs@conduktor.io!

We're hiring full-remote Front-end Developers experimented with React and Typescript, with an interest in beautiful UIs, able to think as a user (UX), and used to work with backend teams (Scala here).

More details: https://www.conduktor.io/jobs/

# The Challenge

Conduktor is a software company centered around Apache Kafka.
Apache Kafka is _basically_ a message broker. It forms a _cluster_ composed of many _topics_ containing _data_.

Conduktor is making the work and monitoring of Apache Kafka more visible and friendly.

## Build a mini-Conduktor

We'd like you to create a tiny version of our software where we could:
- register/login (using Auth0, see below)
- create/list clusters and their topics
- fetch data from topics (in "real-time")

This is a Front-end challenge: it should be friendly to use.

## The project

You must create a front-end project using:

- React v17+
- TypeScript 4.3+ (⚠️ we do NOT code using JavaScript)
- Ant Design (or better) for the UI components
- We'll provide you an OpenAPI specification to work with (to simulate a backend, see below)

## Requirements

- We should be able to login/logout using an Auth0 integration
  - [checkout their documentation](https://auth0.com/docs/quickstart/spa/react/01-login) for the integration
  - We provide you a sandbox (see below)
  - This will automatically provide the front-end a JWT with user information
- Display the name/picture from the JWT token in the application (with a logout menu)
- I should be able to create clusters & topics (see below for the contract)
- I should be able to switch the locale in the application without screen full-refresh
  - eg: English, French (or your native language!)
- If I open the application in multiple tabs: they must be synchronized
  - eg1: if I create a resource on tab A, I should see it on tab B
  - eg2: if I logout on tab A, it should logout on tab B

## Contract sample

Here is a simple view of the [OpenAPI](openapi.yaml) you have to work with:

- `GET /clusters`: list the clusters
- `POST /clusters`: create a cluster
- `GET /clusters/:clusterId/topics`: list the topics of the cluster
- `POST /clusters/:clusterId/topics`: create a topic in this cluster
- `GET /clusters/:clusterId/topics/:topic/data`: you should generate random data here (to simulate a backend)
  - SSE, these are real-time data!

We don't provide any backend server, you will have to mock the OpenAPI.

## Auth0 Authentication

You can create your own Auth0 sandbox or use this one for the coding challenge:

- Domain: `conduktor-coding-challenge.eu.auth0.com`
- ClientID: `2BczaMeSZzUhOfRfDOFG5QXcfaXQUjmE`
- Callback & Logout URL we've configured: `http://localhost:8000`

Don't hesitate to ask us if you need something here.

## How long?

Time estimated: it depends on you!

It's really the "job" at Conduktor, just think that it's your onboarding. :-)

Before submitting your challenge, make sure all the above requirements are okay or find a good reason why it's not. :-)
