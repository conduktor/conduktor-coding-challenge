# We're hiring Front-end Developers! 👨‍💻 👩‍💻

Don't hesitate to do the challenges presented here and tell us: jobs@conduktor.io!

We're hiring full-remote Front-end Developers experimented with React and Typescript, with an interest in beautiful UIs, able to think as a user (UX), and used to work with backend teams (Scala here).

- Job description to read: [Front-End Developer](https://jobs.lever.co/conduktor/7fcba886-ff74-4e08-a76d-de9c51e5c838).
- Please read this if you want to apply: [How our Application process works?](../application-process.md). This is necessary to ensure your application process will be smooth.

# The Challenge

Conduktor is a software company centered around Apache Kafka.
Apache Kafka is _basically_ a message broker. It has _topics_ containing _data_. Any application can send data to Apache Kafka, and other applications can "listen" to these incoming data.

### Vocabulary

- Topics are a way to organize messages in Apache Kafka. Each topic has a name that is unique across the entire Kafka cluster.
- Producers write data to topics, and consumers read data from topics. (it's a Pub/Sub system)

## Business requirements: a mini-Conduktor

Create a SPA where we can:

- register/login/logout (we provide you an Auth0 sandbox, see below)
- display our identity (name/photo) in the application header (`useAuth0()` using `auth0-react`)
- create a topic with a name
- list topics
- click on a topic to consume its data in real-time (data are flowing!)
  - You can take a peek at how it works today: https://youtu.be/zB9tsZN8Fbs?list=PLYmXYyXCMsfMMhiKPw4k1FF7KWxOEajsA&t=96
- use a state (react context or redux) to save a locale, and retrieve it in a component (no need to setup i18n libs, we're just validating state usage)

## Technical requirements

- TypeScript 4.3+ (no JavaScript)
- React v17+, hooks, React-router, manage forms, manage state
- Use GraphQL (either Apollo Client or @tanstack/react-query), that's what we are using for all our products.
- Use the UI library you want

## Design Inspiration

- Our desktop product (list of topics that we can "consume" messages from):

<img src="https://user-images.githubusercontent.com/3936459/129449736-1f953556-30e9-44af-b753-fab8806fde69.png" width=500 />

Don't try to reproduce it exactly, it's just to get you an idea of what is a list of topics!

- You can also check [this sketch example](./design_example.excalidraw.png) (feel free to derive or propose a completely different solution)

## Handle the Login part using Auth0

You can follow [the official example](https://auth0.com/docs/quickstart/spa/react/01-login).
You can create your own Auth0 sandbox OR use this one:

- Domain: `conduktor-coding-challenge.eu.auth0.com`
- ClientID: `2BczaMeSZzUhOfRfDOFG5QXcfaXQUjmE`
- Callback & Logout URL we've configured: `http://localhost:8000`

## Server

We provide a nodejs server, [see here for the instructions](./server/).
Introspection is enabled. Routes are not authenticated (to let you explore freely) but we expect the token to be passed in headers

### Bonus :

Production mode : use the --flaky mode on the server. It will fail randomly, forcing you to handle errors 🦹 (think UX)

## How long?

Time estimated: from a few hours to a workday

It's really the "job" at Conduktor, just think that it's your onboarding. :-)

Before submitting your challenge, make sure all the above requirements are okay or find a good reason why it's not and explain what you would do in details.
