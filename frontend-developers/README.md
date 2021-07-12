# We're hiring Front-end Developers! 👨‍💻 👩‍💻

Don't hesitate to do the challenges presented here and tell us: jobs@conduktor.io!

We're hiring full-remote Front-end Developers experimented with React and Typescript, with an interest in beautiful UIs, able to think as a user (UX), and used to work with backend teams (Scala here).

More details: https://www.conduktor.io/jobs/

> Fork this repository privately, then send the link to jobs@conduktor.io for us to discuss!

# The Challenge

Conduktor is a software company centered around Apache Kafka.
Apache Kafka is _basically_ a message broker. It forms a _cluster_ composed of many _topics_ containing _data_.

Conduktor is making the work and monitoring of Apache Kafka more visible and friendly.

## Goal: Build a mini-Conduktor

We'd like you to create a tiny version of our software where we could:
- register/login
- create/list clusters and their topics
- fetch data from topics (in "real-time")

This is a Front-end challenge: it should be friendly to use.

## Technical Details

You must create a front-end project using:

- React v17+
- TypeScript 4.3+ (⚠️ we do NOT code using JavaScript)
- Ant Design (or better) for the UI components
- We provide you an OpenAPI specification to simulate the backend, see below

## Business Requirements

- We should be able to login/logout using an Auth0 integration
  - We provide you a sandbox (see below)
  - This will automatically provide the front-end a JWT with user information
- Display the name/picture from the JWT token in the application (with a logout menu)
- I should be able to create clusters & topics (see below for the contract)
- I should be able to switch the locale in the application without screen full-refresh
  - eg: English, French (or your native language!)
- Bonus: If I open the application in multiple tabs: they must be synchronized
  - eg1: if I create a resource on tab A, I should see it on tab B
  - eg2: if I logout on tab A, it should logout on tab B

## The OpenAPI specification to use for this challenge

Here is an overview of the [OpenAPI](openapi.yaml) you have to work with:

- `GET|POST /clusters`: list and create clusters
- `GET|POST /clusters/:clusterId/topics`: list and create topics
- `GET      /clusters/:clusterId/topics/:topic/data`: get _real-time_ data from a topic
  - Using SSE: these are real-time data emit by Apache Kafka

We don't provide you any backend server, you can mock using the OpenAPI specification.

## Handle the Login part using Auth0

To easily integrate auth0, [checkout their documentation and example](https://auth0.com/docs/quickstart/spa/react/01-login).

You can create your own Auth0 sandbox or use this one for the coding challenge:

- Domain: `conduktor-coding-challenge.eu.auth0.com`
- ClientID: `2BczaMeSZzUhOfRfDOFG5QXcfaXQUjmE`
- Callback & Logout URL we've configured: `http://localhost:8000`

Don't hesitate to ask us if you need something here.

## How long?

Time estimated: it depends on you!

It's really the "job" at Conduktor, just think that it's your onboarding. :-)

Before submitting your challenge, make sure all the above requirements are okay or find a good reason why it's not. :-)

> Fork this repository privately, then send the link to jobs@conduktor.io for us to discuss!
