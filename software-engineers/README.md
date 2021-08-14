# We're hiring Scala/Kafka Software Engineers! 👨‍💻 👩‍💻

Don't hesitate to do the challenges presented here and tell us: jobs@conduktor.io!

We're hiring Software Engineers familiar with the Apache Kafka ecosystem (as Developers & Ops) and Scala/ZIO.

- Job description to read: [Software Engineers](https://apply.workable.com/conduktor/j/A7E3C47339/).
- Please read this if you want to apply: [How our Application process works?](../application-process.md). This is necessary to ensure your application process will be smooth.

# The Challenge

Conduktor is a software company centered around Apache Kafka.

## Business requirements: a mini-Conduktor

Write an application that displays records flowing in *real-time* from a topic.

> Today, Conduktor is a rich (heavy/thick) client written in Kotlin & Scala & JavaFX without HTTP API. For this challenge, you can either follow this pattern or if you know React, you can write a Front-end + a Scala API (http4s/ZIO).

- a module/webapp for the UI
  - with React if you know
  - with [tornadofx](https://github.com/edvin/tornadofx) (Kotlin) or [scalafx](https://www.scalafx.org/)
- a Scala/ZIO module/API to deal with Apache Kafka (connect, list topics, consume records...)

### I should be able to

- set a Kafka bootstrap address
- add additional properties to pass to the KafkaAdmin & KafkaConsumer (security etc.)
- view all the topics
- select a topic and consume its data from the beginning
- see the records flowing without the UI to be stuck (and in real-time)
- stop the consumption, select another topic, then consume it etc.

### Technical requirements

- Only sbt or gradle, no Maven
- Use JDK 11+ or more. (no JDK 8 please) (you may use the branch `jdk10` of tornadofx if you're using it)
- Apache Kafka: Do NOT use consumer groups but custom partition assignments (no group id should be used)
- JavaFX: Do NOT use FXML but plain code for views.

## Design Inspiration

Our existing product:

<img src="https://user-images.githubusercontent.com/3936459/129449736-1f953556-30e9-44af-b753-fab8806fde69.png" width=500 />

### How long?

Time estimated: it depends on you!

It's really the "job" at Conduktor, just think that it's your onboarding. :-)

## Comment the code

Review the [code-comments](https://github.com/conduktor/conduktor-coding-challenge/tree/main/software-engineers/code-comments) and tell us what do you think of them.

# If you use Kotlin

Here are additional stuff you should be using with Kotlin:

- [Coroutines](https://kotlinlang.org/docs/reference/coroutines-overview.html): don't use Threads to do async stuff. Coroutine are like Fibers, can scale massively without impact and provide automatic supervision (parent-child relationships).
- [Flow](https://kotlinlang.org/docs/reference/coroutines/flow.html): equivalent of RxJava, Reactor, Akka Streams, ZIO Streams etc. in Kotlin.
- [Arrow](https://arrow-kt.io/): the Functional companion to Kotlin's Standard Library (Either, Validated, traverse, etc.)
- Scala/Kotlin interop to write: ZStreams -> Flow, ZIO -> Coroutine.


