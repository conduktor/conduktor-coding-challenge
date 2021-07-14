# We're hiring Front-end Developers! 👨‍💻 👩‍💻

Don't hesitate to do the challenges presented here and tell us: jobs@conduktor.io!

We're hiring full-remote Front-end Developers experimented with React and Typescript, with an interest in beautiful UIs, able to think as a user (UX), and used to work with backend teams (Scala here).

# 1. The Job requirements

Please confirm that you fit our position: [Front-End Developer](https://apply.workable.com/conduktor/j/5F3415C656/).

# 2. The Application Process

Please read this if you want to apply: [How our Application process works?](../application-process.md).

This is necessary to ensure your application process will be smooth.

# 3. The Challenge

Conduktor is a software company centered around Apache Kafka.
Apache Kafka is _basically_ a message broker. It forms a _cluster_ composed of many _topics_ containing _data_. Any application can send data to Apache Kafka, and other applications can "listen" to these incoming data.

## Business requirements: Build a mini-Conduktor

We'd like you to create a tiny version of our software where we could:
- register/login/logout (we provide you an Auth0 sandbox, see below)
- display our identity in the application (using the JWT given by Auth0)
- create/list clusters and their topics
- fetch (mock) data from topics in "real-time" (SSE)

This is a Front-end challenge: it should be user-friendly to use.

## Technical Details

You must create a front-end project using:

- React v17+
- TypeScript 4.3+ (⚠️ we do NOT code using JavaScript)
- Ant Design (or better) for the UI components
- We provide you an OpenAPI specification to simulate the backend, see below

## The OpenAPI specification to use for this challenge

Check the [openapi.yaml](openapi.yaml) you have to work with (just mock it), and below its quick overview:

- GET and POST `/clusters`: list and create clusters
- GET and POST `/clusters/:clusterId/topics`: list and create topics
- GET `/clusters/:clusterId/topics/:topic/data`: fetch _real-time_ data from a topic (using SSE). Just mock the data randomly.

## Handle the Login part using Auth0

To manage the login/logout part using Auth0, [follow their documentation and example](https://auth0.com/docs/quickstart/spa/react/01-login).
You can create your own Auth0 sandbox OR use this one:

- Domain: `conduktor-coding-challenge.eu.auth0.com`
- ClientID: `2BczaMeSZzUhOfRfDOFG5QXcfaXQUjmE`
- Callback & Logout URL we've configured: `http://localhost:8000`

Don't hesitate to ask us if you need some more configuration here.

### Optional

In production, we will also ask you to implement these features, so you can give a try:

- I should be able to switch the locale in the application without screen full-refresh
  - eg: English, French (or your native language!)
- Extra (will be mandatory in production): If I open the application in multiple tabs: they must be synchronized
  - eg1: if I create a resource on tab A, I should see it on tab B
  - eg2: if I logout on tab A, it should logout on tab B
  
## How long?

Time estimated: a few hours

It's really the "job" at Conduktor, just think that it's your onboarding. :-)

Before submitting your challenge, make sure all the above requirements are okay or find a good reason why it's not and explain what you would do in details.
