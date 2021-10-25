# We're hiring Front-end Developers! 👨‍💻 👩‍💻

Don't hesitate to do the challenges presented here and tell us: jobs@conduktor.io!

We're hiring full-remote Front-end Developers experimented with React and Typescript, with an interest in beautiful UIs, able to think as a user (UX), and used to work with backend teams (Scala here).

- Job description to read: [Front-End Developer](https://apply.workable.com/conduktor/j/5F3415C656/).
- Please read this if you want to apply: [How our Application process works?](../application-process.md). This is necessary to ensure your application process will be smooth.

# The Challenge

Conduktor is a software company centered around Apache Kafka.
Apache Kafka is _basically_ a message broker. It has _topics_ containing _data_. Any application can send data to Apache Kafka, and other applications can "listen" to these incoming data.

## Business requirements: a mini-Conduktor

Create a SPA where we can:

- register/login/logout (we provide you an Auth0 sandbox, see below)
- display our identity (name/photo) in the application (`useAuth0()` using `auth0-react`)
- create/list topics
- click on a topic to consume data from it in real-time (data are flowing!)
- switch the Locale of the application (using React Context)

## Technical requirements

- React v17+, hooks etc.
- TypeScript 4.3+ (no JavaScript)
- Ant Design
- To fetch the topics and the data, build a quick and dirty REST API or or use an online mock service

## Design Inspiration

Our existing product (list of topics that we can "consume" messages from):

<img src="https://user-images.githubusercontent.com/3936459/129449736-1f953556-30e9-44af-b753-fab8806fde69.png" width=500 />

Don't try to reproduce it exactly, it's just to get you an idea of what is a list of topics!

## Handle the Login part using Auth0

You can follow [the official example](https://auth0.com/docs/quickstart/spa/react/01-login).
You can create your own Auth0 sandbox OR use this one:

- Domain: `conduktor-coding-challenge.eu.auth0.com`
- ClientID: `2BczaMeSZzUhOfRfDOFG5QXcfaXQUjmE`
- Callback & Logout URL we've configured: `http://localhost:8000`

### Bonus

Synchronize the state if multiple tabs are opened:

- eg1: if I logout on tab A, it should logout on tab B
- eg2: if I create a resource on tab A, I should see it on tab B
  
## How long?

Time estimated: a few hours

It's really the "job" at Conduktor, just think that it's your onboarding. :-)

Before submitting your challenge, make sure all the above requirements are okay or find a good reason why it's not and explain what you would do in details.
